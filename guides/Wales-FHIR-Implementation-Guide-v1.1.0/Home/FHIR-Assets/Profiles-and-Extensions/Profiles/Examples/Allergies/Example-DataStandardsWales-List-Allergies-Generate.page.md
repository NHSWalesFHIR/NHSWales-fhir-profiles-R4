<div class="warning"><span class="ClinicalWarn"></span></div>

## Example List Allergies (generate)

This example references the following example resources:
* Allergies:
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Allergies/Example-DataStandardsWales-AllergyIntolerance-Morphine.page.md, text: morphine}}  - following modification from degraded to be coded correctly
   * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Allergies/Example-DataStandardsWales-AllergyIntolerance-Potato.page.md, text:Potato}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Allergies/Example-DataStandardsWales-AllergyIntolerance-Ibuprofen.page.md, text: Ibuprofen}} - following modification from degraded to be coded correctly
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Allergies/Example-DataStandardsWales-AllergyIntolerance-Wasps.page.md, text: wasp}} - following modification from degraded to be coded correctly
* Subject, source and context:
  * {{pagelink:Example-DataStandardsWales-Patient-AliceJones, text:Patient - Alice Jones}}
  * {{pagelink:Example-DataStandardsWales-Practitioner-Consultant, text:Practitioner - Dr Dhiren Patel }}


<div class="tab-wrap">
  <ul class="tab-head">
    <li class="tablink" onclick="openCity(this,'tabtree')" data-target="tabtree">
      Overview
    </li>
    <li class="tablink" onclick="openCity(this,'tabtable')" data-target="tabtable">
      Table
    </li>
    <li class="tablink tab-active" onclick="openCity(this,'tabxml')" data-target="tabxml">
      XML
    </li>    
    <li class="tablink" onclick="openCity(this,'tabjson')" data-target="tabjson">
      JSON
    </li>    

  </ul>
  <div class="tab-main">
    <div id="tabtree" class="tabcontent">
      {{tree:fhir-standards-wales/example-datastandardswales-bundle-allergies-upgrade}}
    </div>
    <div id="tabtable" class="tabcontent">
      {{table:fhir-standards-wales/example-datastandardswales-bundle-allergies-upgrade}}
    </div>       
    <div id="tabxml" class="tabcontent active">      
      {{xml:fhir-standards-wales/example-datastandardswales-bundle-allergies-upgrade}}
    </div>
    <div id="tabjson" class="tabcontent">
      {{json:fhir-standards-wales/example-datastandardswales-bundle-allergies-upgrade}}
    </div>       
  </div>
</div>