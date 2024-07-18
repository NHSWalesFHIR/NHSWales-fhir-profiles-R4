<div class="warning"><span class="ExperiWarn"></span></div>

## {{page-title}}
The [DiagnosticReport](https://www.hl7.org/fhir/r4/DiagnosticReport.html) profile contains findings and interpretation of diagnostic tests performed on patients, groups of patients, devices, and locations, and/or specimens derived from these. The report includes clinical context such as requesting and provider information, and some mix of atomic results, images, textual and coded interpretations, and formatted representation of diagnostic reports.

A direct link to the Data Standards Wales asset can be accessed here - {{link:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-DiagnosticReport}}

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
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-DiagnosticReport, snapshot}}
    </div>
    <div id="tabdiff" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-DiagnosticReport, diff}}
  </div>
    <div id="tabhybrid" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-DiagnosticReport, hybrid}}
  </div>
  <div id="tabeg" class="tabcontent">
    <list>
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
1. A code describing the type of report
1. A patient

**Each DiagnosticReport must support:**
1. The encounter the report occurred within
1. A category
1. An effective timestamp
1. An issued date for this report version
1. An author (actor) producing the report
1. A reference to one or more specimens
1. A reference to one or more test results
1. A reference to one or more images
1. A reference to the full report (presentedForm)

*see Implementation Guidance for the identifier element below

### Implementation Guidance

* The `DiagnosticReport.status` field **SHALL** be populated to indicate whether the report is preliminary, partial, final.
<br><br>
* The `DiagnosticReport.code` field **SHALL** be populated.
<br><br>
* Depending on the report type the `DiagnosticReport.result`, `DiagnosticReport.imagingStudy` or `DiagnosticReport.presentedForm` **SHALL** be populated according to guidance set out in the [Diagnostic Reports Guidance page](https://simplifier.net/guide/FHIR-Standards-Wales-Implementation-Guide/Home/Guidance/Diagnostic-Reports?version=current).
<br><br>
* The `DiagnosticReport.identifier` field **SHOULD** contain all available identifiers. Typical identifiers include:
  * Identifiers assigned to the DiagnosticReport by the Welsh Results and Reporting Service
  * Other identifiers assigned by a hospital PAS or other clinical system.
<br><br>
* The `DiagnosticReport.category` field **SHOULD** be populated. E.g.:
  * RAD - (Radiology)
  * MB - (Microbiology)
<br><br>
* The `DiagnosticReport.effective` field **SHOULD** be populated. The diagnostically relevant time (known as the “effective time” and typically the time of the procedure)*
<br><br>
* The `DiagnosticReport.issued` field **SHOULD** be populated. The time this version of the report was made available*
<br><br>


### Example DiagnosticReports
The following example resources are provided within this guide: 

 - {{pagelink:Example-DataStandardsWales-DiagnosticReport-CTAbdomen, text: Radiology - CT Abdomen}}
 - {{pagelink:Example-DataStandardsWales-DiagnosticReport-ECG, text: Cardiology - ECG}}
 - {{pagelink:Example-DataStandardsWales-DiagnosticReport-StressTest, text: Cardiology - Stress Test}}

 * Please see [Data Standards Wales DiagnosticReport Profile for Laboratory results]{{pagelink:DataStandardsWales-DiagnosticReport-Lab}} for examples of Pathology/Laboratory results.
      

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
    
    1. `GET [base]/DiagnosticReport?Patient=Patient/23&category=https://fhir.nhs.wales/Id/wrrs-provider-type-code|P&date=ge2010-01-14T00:00:00Z`
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