<div class="warning"><span class="ImplementWarn"></span></div>

## {{page-title}}
The [MedicationStatement](https://www.hl7.org/fhir/r4/medicationstatement.html) resource is a record of a medication that is being consumed by a patient..

The {{page-title}} profile is derived from the [UK Core MedicationStatement Profile](https://simplifier.net/guide/uk-core-implementation-guide/Home/ProfilesandExtensions/ProfileUKCore-MedicationStatement?version=1.0.0). It defines additional rules for use within health and care organisations in Wales.

For additional guidance on implementation of UK Core, [see here](https://simplifier.net/guide/UK-Core-Implementation-Guide/Home?version=1.0.0).

A direct link to the Data Standards Wales asset can be accessed here - {{link:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-MedicationStatement}}

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
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-MedicationStatement, snapshot}}
    </div>
    <div id="tabdiff" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-MedicationStatement, diff}}
  </div>
    <div id="tabhybrid" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-MedicationStatement, hybrid}}
  </div>
  <div id="tabeg" class="tabcontent">
    <list>
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/Example-DataStandardsWales-MedicationStatement-Amoxi.-Infusion.page.md, text:Amoxicillin (infusion)}}</li> 
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Inpatient/Example-DataStandardsWales-MedicationStatement-Ramipr.-Inpatient.page.md, text:Ramipril}}</li>
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Admission/Example-DataStandardsWales-MedicationStatement-Ibupro.-Admission.page.md, text:Ibuprofen}}</li>                
    </list>
  </div>    
</div>

### Mandatory and Must Support Data Elements
Refer to the {{pagelink:Home/Introduction/Profile-Descriptions/Mandatory-and-Must-Support-Data-Elements.page.md,text: Mandatory and Must Support}} page for guidance on how these elements should be interpreted.
 
Each MedicationStatement must have:
1. A status
2. A code to indicate the medication or reference to a medication record
3. A subject 

Each MedicationStatement must support:
1. A category
2. A context (i.e. a reference to the encounter)
3. The date asserted
4. The information source
5. Dosage information
6. An indication of the course of therapy type (e.g. repeat or acute)

### Extensions

The extensions listed below are those created to support Data Standards Wales: 
  
* The {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Extensions/Extension-DataStandardsWales-MedicationCourseOfTherapyType.page.md,text:DataStandardsWales-MedicationCourseOfTherapyType}} extension is used to indicate the overall pattern of medication administration at the MedicationStatement level (e.g. repeat or acute). This provides addition context to a clinician reviewing a list of patient medications to determine the reason why a patient is taking a medication, and **SHOULD** be populated if this data exists within the communicating system.