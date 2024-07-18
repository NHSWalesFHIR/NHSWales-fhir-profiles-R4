<div class="warning"><span class="ExperiWarn"></span></div>

## {{page-title}}

The **Data Standards Wales DiagnosticReport-Lab** profile (based on [DiagonsticReport](https://www.hl7.org/fhir/r4/DiagnosticReport.html)) is used to represent Laboratory Result Reports (e.g. Clinical Chemistry, Haematology, Microbiology, etc.). The results of such tests are typically contained within nested panels of results (such as a Full Blood Count or Liver Function Test panel) which are represented by Observation resources that contain references to other nested Observations. 

The purpose of this profile is to provide a set of guidelines and minimum standards to allow DiagnosticReport resources to be used to record, search, and fetch laboratory results associated with a patient in a consistent and interoperable manner.

A direct link to the Data Standards Wales asset can be accessed here - {{link:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-DiagnosticReport-Lab}}

The diagram below shows the typical structure of a Laboratory Result Report.

{{render:Diagrams-Diagram-DiagnosticReport-MultiplePanel}}

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
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-DiagnosticReport-Lab, snapshot}}
    </div>
    <div id="tabdiff" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-DiagnosticReport-Lab, diff}}
  </div>
    <div id="tabhybrid" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-DiagnosticReport-Lab, hybrid}}
  </div>
  <div id="tabeg" class="tabcontent">
    <list>
      <li>{{pagelink:Example-DataStandardsWales-DiagnosticReport-FBC, text: Pathology - Full Blood Count}}</li>
      <li>{{pagelink:Example-DataStandardsWales-DiagnosticReport-MultiplePanel, text: Multiple Panel: ACE (Angiotensin Converting Enzyme), LFT (Liver Function Test)}}</li>
      <li>{{pagelink:Example-DataStandardsWales-DiagnosticReport-CTAbdomen, text: Radiology - CT Abdomen}}</li>
      <li>{{pagelink:Example-DataStandardsWales-DiagnosticReport-ECG, text: Cardiology - ECG}}</li>
      <li>{{pagelink:Example-DataStandardsWales-DiagnosticReport-StressTest, text: Cardiology - Stress Test}}</li>
      
    </list>
  </div>    
</div>

### Mandatory and Must Support Data Elements
Refer to the {{pagelink:Home/Introduction/Profile-Descriptions/Mandatory-and-Must-Support-Data-Elements.page.md,text: Mandatory and Must Support}} page for guidance on how these elements should be interpreted.
 
**Each DiagnosticReport must have:**
1. A status
1. A category of LAB *
1. A code describing the type of report
1. A patient

**Each DiagnosticReport must support:**
1. A local or business identifier for the report
1. An encounter
1. An effective timestamp
1. An issued date for this report version
1. A performer
1. Specimen(s)
1. Test results(s)

*see Implementation Guidance for the identifier element below

### Implementation Guidance
* The `DiagnosticReport.identifier` field **SHOULD** contain all available identifiers. Typical identifiers include:
  * Identifiers assigned to the DiagnosticReport by the Welsh Results and Reporting Service
  * Other identifiers assigned by a hospital PAS or other clinical system.
* The `DiagnosticReport.status` field **SHALL** be populated to indicate whether the report is preliminary, partial, final.
* The `DiagnosticReport.category` field **SHALL** be populated with a category code of LAB. Note that it is possible to include additional category codes.
* The `DiagnosticReport.code` field **SHALL** be populated.
* For laboratory reports, the `DiagnosticReport.subject` field **SHALL** contain reference to a patient resource. References to other resource types are not permissible.
* The `DiagnosticReport.encounter` field **SHOULD** contain a reference to the encounter associated with the test report if this data is available.
* The `DiagnosticReport.effective` field **SHOULD** be populated. The diagnostically relevant time (known as the “effective time” and typically the time of the procedure)*
* When results become available, the `DiagnosticReport.result` field will include panels of results (such as a Full Blood Count or Liver Function Test panel) which are represented by observation resources that contain references to other nested Observations. Such observations and contained nested observations will implement the [Data Standards Wales Observation Lab]({{pagelink:DataStandardsWales-Observation-Lab}}) profile.
* The `DiagnosticReport.issued` field **SHOULD** be populated. The time this version of the report was made available*
<br><br>


### Example DiagnosticReports
The following example resources are provided within this guide: 

 - {{pagelink:Example-DataStandardsWales-DiagnosticReport-FBC, text: Pathology - Full Blood Count}}
 - {{pagelink:Example-DataStandardsWales-DiagnosticReport-MultiplePanel, text: Multiple Panel: ACE (Angiotensin Converting Enzyme), LFT (Liver Function Test)}}
      

### Mandatory Search Parameters
The following search parameters and search parameter combinations **SHALL** be supported:
1. **SHALL** support searching by an DiagnosticReport identifier using the `identifier` search parameter:
    ```
    GET [base]/DiagnosticReport?identifier={system|}[code]
    ```
    Example:
    1. `GET [base]/DiagnosticReport?identifier=https://fhir.nhs.wales/Id/wrrs-report-identifier|1000122`
<br>
_Implementation Notes:_ Fetches a bundle containing any DiagnosticReport resources matching the identifier ([how to search by token](http://hl7.org/fhir/R4/search.html#token)).
<br><br>
1. **SHALL** support searching using  the `patient` search parameter:
    ```
    GET [base]/DiagnosticReport?patient={Type/}[id]
    ```
    Example:
    1. `GET [base]/DiagnosticReport?patient=Patient/NN046351-149`  
    1. `GET [base]/DiagnosticReport?patient:identifier=https://fhir.nhs.uk/Id/nhs-number|9912003444`
<br>
_Implementation Notes:_ Fetches a bundle of all DiagnosticReport resources for the specified patient ([how to search by reference](http://hl7.org/fhir/R4/search.html#reference))
<br><br>
1. **SHALL** support searching using the combination of the `patient` and `code` search parameters:
    
    * including optional support for _OR_ search on `code` (e.g.`code={system|}[code],{system|}[code],...`)
    
    ```
    GET [base]/DiagnosticReport?patient={Type/}[id]&code={system|}[code]{,{system|}[code],...}
    ```
    
    Example:
    
    1.  `GET \[base\]/DiagnosticReport?patient=23&code=https://fhir.nhs.wales/Id/wrrs-provider-system-code|FBC`
    1.  `GET \[base\]/DiagnosticReport?patient:identifier=https://fhir.nhs.uk/Id/nhs-number|9912003444&code=https://fhir.nhs.wales/Id/wrrs-provider-system-code|FBC,https://fhir.nhs.wales/Id/wrrs-provider-system-code|LFT`
<br>
_Implementation Notes:_ Fetches a bundle of all DiagnosticReport resources for the specified patient and DiagnosticReport code(s). SHOULD support search by multiple report codes. The DiagnosticReport `code` parameter searches \`DiagnosticReport.code only. ([how to search by reference](http://hl7.org/fhir/R4/search.html#reference) and [how to search by token](http://hl7.org/fhir/R4/search.html#token))

### Optional Search Parameters
The following search parameters and search parameter combinations **SHOULD** be supported:
1.  **SHOULD** support searching using the combination of the `patient` and `status` search parameters:
    
    *   including support for _OR_ search on `status` (e.g.`status={system|}[code],{system|}[code],...`)
    
    ```
    GET [base]/DiagnosticReport?patient={Type/}[id]&status={system|}[code]{,{system|}[code],...}
    ```
    
    Example:
    
    1. `GET \[base\]/DiagnosticReport?patient=23&status=final`    
_Implementation Notes:_ Fetches a bundle of all DiagnosticReport resources for the specified patient and status ([how to search by reference](http://hl7.org/fhir/R4/search.html#reference) and [how to search by token](http://hl7.org/fhir/R4/search.html#token))
<br><br>
1.  **SHOULD** support searching using the combination of the `patient` and `category` and `date` search parameters:
    
    *   including support for these `date` comparators: `gt,lt,ge,le`
    *   including optional support for _AND_ search on `date` (e.g.`date=[date]&date=[date]]&...`)
    
    ```
    GET [base]/DiagnosticReport?patient={Type/}[id]&category={system|}[code]&date={gt|lt|ge|le}[date]{&date={gt|lt|ge|le}[date]&...}
    ```
    
    Example:
    
    1. `GET [base]/DiagnosticReport?Patient=Patient/23&category=http://terminology.hl7.org/CodeSystem/v2-0074|LAB&date=ge2010-01-14T00:00:00Z`
<br>
_Implementation Notes:_ Fetches a bundle of all DiagnosticReport resources for the specified patient and date and a category code specified in Data Standards Wales DiagnosticReport Category Codes ([how to search by reference](http://hl7.org/fhir/R4/search.html#reference) and [how to search by token](http://hl7.org/fhir/R4/search.html#token) and [how to search by date](http://hl7.org/fhir/R4/search.html#date))
<br><br>
1.  **SHOULD** support searching using the combination of the `patient` and `code` and `date` search parameters:
    
    *   including optional support for _OR_ search on `code` (e.g.`code={system|}[code],{system|}[code],...`)
    *   including support for these `date` comparators: `gt,lt,ge,le`
    *   including optional support for _AND_ search on `date` (e.g.`date=[date]&date=[date]]&...`)
    
    ```
    GET [base]/DiagnosticReport?patient={Type/}[id]&code={system|}[code]{,{system|}[code],...}&date={gt|lt|ge|le}[date]{&date={gt|lt|ge|le}[date]&...}
    ```
    
    Example:
    
    1. `GET [base\]/DiagnosticReport?Patient=Patient/23&code=https://fhir.nhs.wales/Id/wrrs-provider-system-code|FBC&date=ge2010-01-14T00:00:00Z`
<br>
_Implementation Notes:_ Fetches a bundle of all DiagnosticReport resources for the specified patient and date and report code(s). ([how to search by reference](http://hl7.org/fhir/R4/search.html#reference) and [how to search by token](http://hl7.org/fhir/R4/search.html#token) and [how to search by date](http://hl7.org/fhir/R4/search.html#date))