<div class="warning"><span class="ExperiWarn"></span></div>

## {{page-title}}
The [Observation](https://www.hl7.org/fhir/r4/Observation.html) resource is used to support diagnosis, monitor progress, determine baselines and patterns and even capture demographic characteristics. Most observations are simple name/value pair assertions with some metadata, but some observations group other observations together logically, or even are multi-component observations. 

Note that the Observations included within an laboratory result report should implement the {{pagelink:DataStandardsWales-Observation-Lab}} profile.

The {{page-title}} profile is derived from the [UK Core STU2 Observation Profile](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Observation?version=current) and is therefore listed as experimental. It defines additional rules for use within health and care organisations in Wales.

A direct link to the Data Standards Wales asset can be accessed here - {{link:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Observation}}

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
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Observation, snapshot}}
    </div>
    <div id="tabdiff" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Observation, diff}}
  </div>
    <div id="tabhybrid" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Observation, hybrid}}
  </div>
  <div id="tabeg" class="tabcontent">
    <list>
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Example-DataStandardsWales-Observation-ACVPU.page.md, text:ACVPU (Alert Confusion Voice Pain Unresponsive) scale score}}</li>
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Example-DataStandardsWales-Observation-BloodPressure.page.md, text:Blood pressure}}</li>
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Example-DataStandardsWales-Observation-BodyHeight.page.md, text:Body height}}</li>
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Example-DataStandardsWales-Observation-BodyTemperature.page.md, text:Body temperature}}</li>
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Example-DataStandardsWales-Observation-BodyWeight.page.md, text:Body weight}}</li>
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Example-DataStandardsWales-Observation-RespiratoryRate.page.md, text:Respiratory rate}}</li>
    </list>
  </div>    
</div>

### Mandatory and Must Support Data Elements
Refer to the {{pagelink:Home/Introduction/Profile-Descriptions/Mandatory-and-Must-Support-Data-Elements.page.md,text: Mandatory and Must Support}} page for guidance on how these elements should be interpreted.
 
**Each Observation must have:**
1. A status
1. A code indicating what is being measured
1. A patient

**Each Observation must support:**
1. An identifier
1. A category code
1. A effective datetime for the observation
1. An interpretation, e.g. high, low, normal

### Example Observations
The following example resources are provided within this guide:
- {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Example-DataStandardsWales-Observation-ACVPU.page.md, text:ACVPU (Alert Confusion Voice Pain Unresponsive) scale score}}, 
- {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Example-DataStandardsWales-Observation-BloodPressure.page.md, text:Blood pressure}}, 
- {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Example-DataStandardsWales-Observation-BodyHeight.page.md, text:Body height}}, 
- {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Example-DataStandardsWales-Observation-BodyTemperature.page.md, text:Body temperature}}, 
- {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Example-DataStandardsWales-Observation-BodyWeight.page.md, text:Body weight}}, 
- {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Example-DataStandardsWales-Observation-RespiratoryRate.page.md, text:Respiratory rate}}.

### Mandatory Search Parameters
The following search parameters and search parameter combinations **SHALL** be supported:

1. **SHALL** support searching using a combination of the `patient` and `category` search parameters:
    ```
    GET [base]/Observation?patient={Type/}[id]&category={system|}[code]
    ```
    Example:
    1. `GET [base]/Observation?patient=23&category=social-history` 
    1. `GET [base]/Observation?patient=23&category=vital-signs` 
    1. `GET [base]/Observation?patient:identifier=https://fhir.nhs.uk/Id/nhs-number|9912003444&category=vital-signs` 
<br>
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
    GET [base]/Observation?patient={Type/}[id]&category={system|}[code]&date={gt|lt|ge|le}[date]{&date={gt|lt|ge|le}[date]&...}
    ```
    Example:
    1. `GET [base]/Observation?patient=23&category=social-history&date=ge2023-01-05T00:00:00Z` 
    1. `GET [base]/Observation?patient:identifier=https://fhir.nhs.uk/Id/nhs-number|9912003444&category=social-history&date=ge2023-01-05T00:00:00Z` 
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