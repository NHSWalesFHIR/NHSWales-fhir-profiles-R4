<div class="warning"><span class="ImplementWarn"></span></div>

## {{page-title}}
The [List](https://www.hl7.org/fhir/r4/list.html) resource is a curated collection of resources. The Medication List profile is intended to provide a snapshot view of a patient's medications.

The {{page-title}} profile is derived from the [UK Core List Profile](https://simplifier.net/packages/fhir.r4.ukcore.stu1/1.0.0/files/806176). It defines additional rules for use within health and care organisations in Wales.

For additional guidance on implementation of UK Core, [see here](https://simplifier.net/guide/UK-Core-Implementation-Guide/Home?version=1.0.0).

A direct link to the Data Standards Wales asset can be accessed here - {{link:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-MedicationList}}

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
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-MedicationList, snapshot}}
    </div>
    <div id="tabdiff" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-MedicationList, diff}}
  </div>
    <div id="tabhybrid" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-MedicationList, hybrid}}
  </div>
  <div id="tabeg" class="tabcontent">
    <list>
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-GP/Example-DataStandardsWales-List-Medications-GP.page.md, text: GP medications list}}</li>
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Outpatient/Example-DataStandardsWales-List-Medications-Outpatient.page.md, text: Outpatient medications list}}</li>      
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Admission/Example-DataStandardsWales-List-Medications-Admission.page.md, text: Medications on admission}}</li>
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Inpatient/Example-DataStandardsWales-List-Medications-Inpatient.page.md, text: Inpatient medications list}}</li>      
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Discharge/Example-DataStandardsWales-List-Medications-Discharge.page.md, text: Medications on discharge}}</li>      
    </list>
  </div>    
</div>

### Mandatory and Must Support Data Elements
Refer to the {{pagelink:Home/Introduction/Profile-Descriptions/Mandatory-and-Must-Support-Data-Elements.page.md,text: Mandatory and Must Support}} page for guidance on how these elements should be interpreted.
 
Each Medication List must have:
1. A status
2. A mode
3. A fixed SNOMED CT code of value of 933361000000108|'Medications and medical devices' *
4. A subject (patient)

_* the list's code is fixed to 'Medications and medical devices' for the current scope of functionality - in further iterations the code field is likely to be bound to a value set of other medication list types_

Each Medication List must support:
1. An encounter
2. A source to indicate who defined the list contents