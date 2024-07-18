<div class="warning"><span class="ImplementWarn"></span></div>

## {{page-title}}

### Overview
The [AllergyIntolerance](https://www.hl7.org/fhir/r4/AllergyIntolerance.html) resource is primarily used to provide a single place with the heath record to document reactions to substance like materials, food or medications. The resource can be used to catalogue reactions to exposures over time including when no reaction takes place at all. The resource can be used to build a catalogue of allergies and intolerances and how they change over time. 

The {{page-title}} profile is derived from the [UK Core AllergyIntolerance Profile](https://simplifier.net/guide/uk-core-implementation-guide/Home/ProfilesandExtensions/ProfileUKCore-AllergyIntolerance?version=1.0.0). It defines additional rules for use within health and care organisations in Wales.

A direct link to the Data Standards Wales asset can be accessed here - {{link:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-AllergyIntolerance}}

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
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-AllergyIntolerance, snapshot}}
    </div>
    <div id="tabdiff" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-AllergyIntolerance, diff}}
  </div>
    <div id="tabhybrid" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-AllergyIntolerance, hybrid}}
  </div>
  <div id="tabeg" class="tabcontent">
    <list>
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Allergies/Example-DataStandardsWales-AllergyIntolerance-Potato.page.md, text:Example food allergy - Potato}}</li>
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Allergies/Example-DataStandardsWales-AllergyIntolerance-deleted.page.md, text:Example deleted allergy - Potato}}</li> 
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Allergies/Example-DataStandardsWales-AllergyIntolerance-NoKnownAllergy.page.md, text:Example exclusion - no known allergy}}</li> 
      <li>{{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Allergies/Example-DataStandardsWales-AllergyIntolerance-Aspirin.page.md, text:Example medication allergy -Aspirin}}</li>                 
    </list>
  </div>    
</div>

### Mandatory and Must Support Data Elements
Refer to the {{pagelink:Home/Introduction/Profile-Descriptions/Mandatory-and-Must-Support-Data-Elements.page.md,text: Mandatory and Must Support}} page for guidance on how these elements should be interpreted.
 
Each AllergyIntolerance must have:
1. A code
1. A patient

Each Encounter must support:
1. A code to indicate clinical status
1. An encounter
1. A recorded date
1. A recorder
1. An asserter
1. Clinical details for reactions recorded for the AllergyIntolerance
1. Evidence *

_*see Implementation Guidance for the evidence extension below_


* The extensions listed below allow a number of the data elements listed above to be supported where not currently supported by the FHIR standard: 
  * UK Core extensions
    * The [UKCore-Evidence](https://simplifier.net/guide/uk-core-implementation-guide/Home/ProfilesandExtensions/ExtensionLibrary?version=1.0.0#ExtensionUKCore-Evidence) extension provides a reference to results of investigations that confirmed the certainty of the diagnosis. Examples might include results of skin prick allergy tests.
* The `AllergyIntolerance.code` field **SHALL** be populated to identify the allergy or intolerance
* The `AllergyIntolerance.patient` field **SHALL** be populated.
