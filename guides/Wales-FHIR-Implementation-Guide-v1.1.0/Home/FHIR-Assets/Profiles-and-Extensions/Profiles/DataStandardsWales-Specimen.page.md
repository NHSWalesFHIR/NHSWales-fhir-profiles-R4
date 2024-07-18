<div class="warning"><span class="ExperiWarn"></span></div>

## {{page-title}}
The [Specimen](https://www.hl7.org/fhir/r4/Specimen.html) resource contains information about a sample to be used for analysis.

The {{page-title}} profile is derived from the [UK Core STU2 Specimen Profile](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Specimen?version=current) and is therefore listed as experimental. It defines additional rules for use within health and care organisations in Wales.

A direct link to the Data Standards Wales asset can be accessed here - {{link:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Specimen}}

### Formal Views of Profile Content
<div class="tab-wrap">
  <ul class="tab-head">
    <li class="tablink tab-active" onclick="openCity(this,'tabsnap')" data-target="tabsnap">
      Snapshot View
    </li>
    <li class="tablink" onclick="openCity(this,'tabdiff')" data-target="tabdiff">
      Differential View
    </li>
    <li class="tablink" onclick="openCity(this,'tabhybrid')" data-target="tabhybrid">
      Hybrid View
    </li>
    <li class="tablink" onclick="openCity(this,'tabeg')" data-target="tabeg">
      Examples
    </li>    
  </ul>
  <div class="tab-main">
    <div id="tabsnap" class="tabcontent active">      
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Specimen, snapshot}}
    </div>
    <div id="tabdiff" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Specimen, diff}}
  </div>
    <div id="tabhybrid" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Specimen, hybrid}}
  </div>
  <div id="tabeg" class="tabcontent">
    <list>
      <li>{{pagelink:Example-DataStandardsWales-Specimen-Blood, text:Example Specimen - Blood}}</li>
      <li>{{pagelink:Example-DataStandardsWales-Specimen-Urine, text:Example Specimen - Urine}}</li>
    </list>
  </div>    
</div>

### Mandatory and Must Support Data Elements
Refer to the {{pagelink:Home/Introduction/Profile-Descriptions/Mandatory-and-Must-Support-Data-Elements.page.md,text: Mandatory and Must Support}} page for guidance on how these elements should be interpreted.
 
**Each Specimen must have:**
1. A Type coding defining what the specimen is *
1. A patient/subject reference *

**Each Specimen must support:**
1. An identifier *
1. A container
1. A receivedTime
1. A request reference
1. A collection datetime

*see Implementation Guidance for the identifier element below

### Implementation Guidance
* The `Specimen.type` field **SHALL** be populated.
* The `Specimen.subject` reference field **SHALL** be populated.
<br><br>
* The `Specimen.identifier` field **SHOULD** contain all available identifiers. Typical identifiers include:
  * Identifiers assigned to the Specimen by the Welsh Results and Reporting Service

### Example Specimens
The following example resources are provided within this guide:
{{pagelink:Example-DataStandardsWales-Specimen-Blood, text:Example Specimen - Blood}}, 
{{pagelink:Example-DataStandardsWales-Specimen-Urine, text:Example Specimen - Urine}}

### Mandatory Search Parameters
The following search parameters and search parameter combinations **SHALL** be supported:
1. **SHALL** support fetching a Specimen using the `_id` search parameter:
    
    ```
    GET [base]/Specimen[id]
    ```
    
    Example:
    - `GET \[base\]/Specimen/500011819107`
    - `GET \[base\]/Specimen?\_id=500011819107`
    
    _Implementation Notes:_ ([how to search by the logical id](http://hl7.org/fhir/R4/references.html#logical) of the resource)

1. **SHALL** support searching using the combination of the `patient` and `type` search parameters:
    
    *   including optional support for _OR_ search on `type` (e.g.`type={system|}[type],{system|}[type],...`)
    
    ```
    GET [base]/Specimen?patient={Type/}[id]&type={system|[type]{,{system|}[type],...}
    ```
    
    Example:
    - `GET \[base\]/Specimen?patient=Patient/NN046351-149&type=https://fhir.nhs.wales/Id/wrrs-specimen-type-code|blood`
    
    _Implementation Notes:_ Fetches a bundle of all Specimen resources for the specified patient and specimen type(s). SHOULD support search by multiple specimen types. ([how to search by reference](http://hl7.org/fhir/R4/search.html#reference) and [how to search by token](http://hl7.org/fhir/R4/search.html#token))

### Optional Search Parameters
The following search parameters and search parameter combinations **SHOULD** be supported:
1. **SHOULD** support searching using the combination of the `patient` and `type` and `collected` search parameters:
    
    *   including optional support for _OR_ search on `type` (e.g.`type={system|}[type],{system|}[type],...`)
    *   including support for these `collected` comparators: `gt,lt,ge,le`
    *   including optional support for _AND_ search on `collected` (e.g.`collected=[date]&collected=[date]]&...`)
    
    ```
    GET [base]/Specimen?patient={Type/}[id]&type={system|[type]{,{system|}[type],...}&collected={gt|lt|ge|le}[date]{&collected={gt|lt|ge|le}[date]&...}
    ```
    
    Example:
    - `GET \[base\]/Specimen?patient=Patient/NN046351-149&type=https://fhir.nhs.wales/Id/wrrs-specimen-type-code|blood&collected=ge2019-01-14T00:00:00Z`
    
    _Implementation Notes:_ Fetches a bundle of all Specimen resources for the specified patient and date and specimen type(s). SHOULD support search by multiple specimen types. ([how to search by reference](http://hl7.org/fhir/R4/search.html#reference) and [how to search by token](http://hl7.org/fhir/R4/search.html#token) and [how to search by date](http://hl7.org/fhir/R4/search.html#date))