<div class="warning"><span class="ExperiWarn"></span></div>

## {{page-title}}

### Overview
The [Encounter](https://www.hl7.org/fhir/r4/encounter.html) resource is used to describe a patient’s attendance at a healthcare facility. Encounters can take place in many forms, such as:
* An emergency or scheduled hospital admission
* An outpatient consultation
* A visit to the GP, or virtual attendance via video link
* Attendance at a mobile breast cancer screening clinic
* Attendance at a mass vaccination centre to receive a vaccination
* A visit from a health care professional to the patient’s home

The {{page-title}} profile is derived from the [UK Core STU2 Encounter Profile](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-Encounter?version=current) and is therefore listed as experimental. It defines additional rules for use within health and care organisations in Wales.

A direct link to the Data Standards Wales asset can be accessed here - {{link:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Encounter}}

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
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Encounter, snapshot}}
    </div>
    <div id="tabdiff" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Encounter, diff}}
  </div>
    <div id="tabhybrid" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Encounter, hybrid}}
  </div>
  <div id="tabeg" class="tabcontent">
    <list>
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Example-DataStandardsWales-Encounter-EmergencyAdmission.page.md, text:Emergency Admission}}</li>     
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Example-DataStandardsWales-Encounter-InProgressEmergencyAdmissio.page.md, text:In-Progress Emergency Admission}}</li>               
    </list>
  </div>    
</div>

### Mandatory and Must Support Data Elements
Refer to the {{pagelink:Home/Introduction/Profile-Descriptions/Mandatory-and-Must-Support-Data-Elements.page.md,text: Mandatory and Must Support}} page for guidance on how these elements should be interpreted.
 
Each Encounter must have:
1. A status
1. A class (e.g. inpatient, emergency etc)

Each Encounter must support:
1. An identifier
1. A subject
1. Participant(s) in the encounter
1. Hospitalization information
1. Admission source
1. Discharge destination
1. Admission method *
1. Discharge method *
1. Emergency care discharge status *
1. Outcome of attendance *

_*see Implementation Guidance on UK Core extensions for the Encounter resource below_

The `Encounter.status` field **SHALL** be populated with one of the following values defined by the FHIR standard:  
  * planned 
  * arrived
  * triaged
  * in-progress
  * onleave
  * finished
  * cancelled
  * entered-in-error
  * unknown
<br><br>
The `Encounter.class` field **SHALL** be populated using the values defined by the FHIR standard

### Extensions
The extensions listed below allow a number of the data elements listed above to be supported where not currently supported by the FHIR standard: 
  * UK Core extensions
    * [UKCore STU2-AdmissionMethod](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/ExtensionLibrary/Extension-UKCore-AdmissionMethod.page.md?version=current) supports the exchange of information representing the method by which a patient was admitted to hospital.
    * [UKCore STU2-DichargeMethod](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/ExtensionLibrary/Extension-UKCore-DischargeMethod.page.md?version=current) supports the exchange of information representing the method by which a patient was discharged from hospital.
    * [UKCore STU2-EmergencyCareDischargeStatus](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/ExtensionLibrary/Extension-UKCore-EmergencyCareDischargeStatus.page.md?version=current) supports the exchange of information representing the status of a patient on discharge from an Emergency Care Department.
    * [UKCore STU2-OutcomeOfAttendance](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/ExtensionLibrary/Extension-UKCore-OutcomeOfAttendance.page.md?version=current) supports the exchange of information representing the outcome of an Outpatient attendance.           
<br><br>
