<div class="warning"><span class="ExperiWarn"></span></div>

## {{page-title}}
The [Observation](https://www.hl7.org/fhir/r4/Observation.html) resource is used to support diagnosis, monitor progress, determine baselines and patterns and even capture demographic characteristics. Most observations are simple name/value pair assertions with some metadata, but some observations group other observations together logically, or even are multi-component observations. Note that the DiagnosticReport resource provides a clinical or workflow context for a set of observations and the Observation resource is referenced by DiagnosticReport to represent laboratory, imaging, and other clinical and diagnostic data to form a complete report.


The **{{page-title}}** profile is derived from the {{pagelink:DataStandardsWales-Observation, text: Data Standards Wales Obervation Profile}} and defines additional rules for use within health and care organisations in Wales.

A direct link to the Data Standards Wales asset can be accessed here - {{link:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Observation-Lab}}

### Profile Inheritance

{{render:Diagrams-Diagram-Observation-DerivedFrom.drawio}}

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
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Observation-lab, snapshot}}
    </div>
    <div id="tabdiff" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Observation-Lab, diff}}
  </div>
    <div id="tabhybrid" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Observation-Lab, hybrid}}
  </div>
  <div id="tabeg" class="tabcontent">
    <list>
      <li>{{pagelink:Example-DataStandardsWales-ObservationGroup-FBC, text: Observation Group - Full Blood Count}}</li>
      <li>{{pagelink:Example-DataStandardsWales-ObservationResult-FBCWBC, text: Observation Result - Whole Blood Count}}</li>
    </list>
  </div>    
</div>

### Mandatory and Must Support Data Elements
Refer to the {{pagelink:Home/Introduction/Profile-Descriptions/Mandatory-and-Must-Support-Data-Elements.page.md,text: Mandatory and Must Support}} page for guidance on how these elements should be interpreted.
 
**Each Observation must have:**
1. A status
1. A category of fixed value laboratory
1. A code, if available, which tells you what is being measured
1. A patient

**Each Observation must support:**
1. An identifier *
1. A category code
1. A effective datetime for the observation
1. A result value or a reason why the data is absent*
1. A reference to one or more specimens
1. A reference to one or more test results

*see Implementation Guidance for the identifier element below

### Implementation Guidance
The DataStandardsWales-Observation profile may be used when presenting an Group or Result Observation resource. An Observation Group or panel, is used to group multiple result sets under an Observation Grouping.

#### Logical Model
{{render:Diagrams-LogicalModel-Observation-Panel.drawio}}

#### Observation Group
* The `Observation.status` field **SHALL** be populated to indicate whether the Observation is Preliminary or Final.
* The `Observation.category` field **SHALL** be populated with a fixed value **laboratory** from the ValueSet http://hl7.org/fhir/ValueSet/observation-category.
* The `Observation.code` field **SHALL** contain all available codes for the requested panel.
  * Codes assigned to the ObservationGroup by the Welsh Results and Reporting Service
  * Other Codes available such as SNOMED CT.
<br/><br/>
* The `Observation.identifier` field **SHOULD** contain all available identifiers. Typical identifiers include:
  * Identifiers assigned to the DiagnosticReport by the Welsh Results and Reporting Service
  * Other identifiers assigned by other clinical system.
* The `Observation.effective` field **SHOULD** be populated. The diagnostically relevant time (known as the “effective time” and typically the time of the procedure)*
* The `Observation.hasMember` field **SHOULD** be populated. The references to all Observation Results for the panel should be available as hasMember references.

#### Observation Result
* The `Observation.status` field **SHALL** be populated to indicate whether the Observation is Preliminary or Final.
* The `Observation.category` field **SHALL** be populated with a fixed value **laboratory** from the ValueSet http://hl7.org/fhir/ValueSet/observation-category.
* The `Observation.code` field **SHALL** contain all available codes for the requested panel.
  * Codes assigned to the ObservationResult by the Welsh Results and Reporting Service
  * Other Codes available such as SNOMED CT.
<br/><br/>
* The `Observation.identifier` field **SHOULD** contain all available identifiers. Typical identifiers include:
  * Identifiers assigned to the DiagnosticReport by the Welsh Results and Reporting Service
  * Other identifiers assigned by other clinical system.
* The `Observation.effective` field **SHOULD** be populated. The diagnostically relevant time (known as the “effective time” and typically the time of the procedure)
* The `Observation.value` field **SHOULD** be populated. The observation result value should be populated if available as **Quantity** resource using the http://unitsofmeasure.org system.
* The `Observation.interpretation` field **SHOULD** be populated. The observation result interpretation should be populated if available using http://hl7.org/fhir/ValueSet/observation-interpretation.
* The `Observation.referenceRange` field **SHOULD** be populated. The observation result referenceRange should be populated if available using the http://unitsofmeasure.org system.

### Mandatory Search Parameters
The following search parameters and search parameter combinations **SHALL** be supported:

1. **SHALL** support searching using a combination of the `patient` and `category` search parameters:
    ```
    GET [base]/Observation?patient={Type/}[id]&category={http://hl7.org/fhir/ValueSet/observation-category|}laboratory
    ```
    Example:
    1. `GET [base]/Observation?patient=23&category=laboratory` 
    1. `GET [base]/Observation?patient:identifier=https://fhir.nhs.uk/Id/nhs-number|9912003444&category=laboratory` 
<br><br>
_Implementation Notes:_ Fetches a bundle of all Observation resources for the specified patient and category. ([how to search by reference](http://hl7.org/fhir/R4/search.html#reference) and [how to search by token](http://hl7.org/fhir/R4/search.html#token))
<br><br>
1. **SHALL** support searching using a combination of the `patient` and `code` search parameters:
    * including optional support for _OR_ search on `code` (e.g. `code={system|}[code],{system|}[code],...`)
    ```
    GET [base]/Observation?patient={Type/}[id]&code={system|}[code]{,{system|}[code],...}
    ```
    Example:
    1. `GET [base]/Observation?patient=23&code=http://snomed.info/sct|75367002` 
    1. `GET [base]/Observation?patient:identifier=https://fhir.nhs.uk/Id/nhs-number|9912003444&code=http://snomed.info/sct|75367002` 
<br>  
_Implementation Notes:_ Fetches a bundle of all Observation resources for the specified patient and code. ([how to search by reference](http://hl7.org/fhir/R4/search.html#reference) and [how to search by token](http://hl7.org/fhir/R4/search.html#token))
<br><br>
1. **SHALL** support searching using a combination of the `patient` and `category` and `date` search parameters:
    * including support for these `date` comparators: `gt,lt,ge,le`
    * including optional support for _AND_ search on `date` (e.g.`date=[date]&date=[date]]&...`)
    ```
    GET [base]/Observation?patient={Type/}[id]&category={http://hl7.org/fhir/ValueSet/observation-category|}laboratory&date={gt|lt|ge|le}[date]{&date={gt|lt|ge|le}[date]&...}
    ```
    Example:
    1. `GET [base]/Observation?patient=23&category=laboratory&date=ge2023-01-05T00:00:00Z` 
    1. `GET [base]/Observation?patient:identifier=https://fhir.nhs.uk/Id/nhs-number|9912003444&category=laboratory&date=ge2023-01-05T00:00:00Z` 
<br>  
_Implementation Notes:_ Fetches a bundle of all MedicationStatement resources for the specified subject and status code. ([how to search by reference](http://hl7.org/fhir/R4/search.html#reference) and [how to search by token](http://hl7.org/fhir/R4/search.html#token) and [how to search by date](http://hl7.org/fhir/R4/search.html#date))
  
### Optional Search Parameters
1. **SHOULD** support searching using the combination of the `patient` and `code` and `date` search parameters:
    * including optional support for _OR_ search on `code` (e.g. `code={system|}[code],{system|}[code],...`) 
    * including support for these `date` comparators: `gt,lt,ge,le`
    * including optional support for _AND_ search on `date` (e.g.`date=[date]&date=[date]]&...`)    
    ```
    GET [base]/Observation?patient={Type/}[id]&code={system|}[code]{,{system|}[code],...}&date={gt|lt|ge|le}[date]{&date={gt|lt|ge|le}[date]&...}
    ```
    
    Example:
    
    1. `GET [base]/Observation?patient=23&code=http://snomed.info/sct|75367002&date=ge2023-01-05T00:00:00Z` 
    1. `GET [base]/Observation?patient:identifier=https://fhir.nhs.uk/Id/nhs-number|9912003444&code=http://snomed.info/sct|75367002&date=ge2023-01-05T00:00:00Z`    
<br>
_Implementation Notes:_ Fetches a bundle of all MedicationStatement resources for the specified subject and status code. ([how to search by reference](http://hl7.org/fhir/R4/search.html#reference) and [how to search by token](http://hl7.org/fhir/R4/search.html#token) and [how to search by date](http://hl7.org/fhir/R4/search.html#date))