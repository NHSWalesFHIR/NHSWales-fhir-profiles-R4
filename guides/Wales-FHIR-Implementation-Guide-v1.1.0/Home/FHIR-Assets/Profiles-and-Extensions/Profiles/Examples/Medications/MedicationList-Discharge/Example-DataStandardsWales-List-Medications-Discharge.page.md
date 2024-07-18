<div class="warning"><span class="ClinicalWarn"></span></div>

## Example Medications List - Discharge medication

This examples medication list is provided as part of a patient journey scenario, which is described {{pagelink:Home/Guidance/Medications/Index.page.md, text:here}}. The list references the following example resources:
* Subject, source and context:
  * {{pagelink:Example-DataStandardsWales-Patient-PeterPiper, text:Patient - Peter Piper}}
* Medication statements:
  * {{pagelink:Example-DataStandardsWales-MedicationStatement-Bendro.-Discharge, text:Bendroflumethiazide}} 
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Discharge/Example-DataStandardsWales-MedicationStatement-Bisop.-Discharge.page.md, text:Bisoprolol}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Discharge/Example-DataStandardsWales-MedicationStatement-Nifedi.-Discharge.page.md, text:Nifedipress}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Discharge/Example-DataStandardsWales-MedicationStatement-Ramipr.-Discharge.page.md, text:Ramipril}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Discharge/Example-DataStandardsWales-MedicationStatement-Atorva.-Discharge.page.md, text:Atorvastatin}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Discharge/Example-DataStandardsWales-MedicationStatement-Parace.-Discharge.page.md, text:Paracetamol}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Discharge/Example-DataStandardsWales-MedicationStatement-Duroge.-Discharge.page.md, text:Durogesic DTrans}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Discharge/Example-DataStandardsWales-MedicationStatement-Hydroc.-Discharge.page.md, text:Hydrocortisone}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Discharge/Example-DataStandardsWales-MedicationStatement-Latano.-Discharge.page.md, text:Latanoprost}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Discharge/Example-DataStandardsWales-MedicationStatement-Enbrel-Discharge.page.md, text:Enbrel}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Discharge/Example-DataStandardsWales-MedicationStatement-Ibupro.-Discharge.page.md, text:Ibuprofen (stopped)}}

Below is an example of the above medication statements combined into a medication list:
  
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
    <li class="tablink" onclick="openCity(this,'tabnarrative')" data-target="tabnarrative">
      Narrative
    </li>
  </ul>
  <div class="tab-main">
    <div id="tabtree" class="tabcontent">
      {{tree:example-datastandardswales-medicationlist-discharge}}
    </div>
    <div id="tabtable" class="tabcontent">
      {{table:example-datastandardswales-medicationlist-discharge}}
    </div>       
    <div id="tabxml" class="tabcontent active">      
      {{xml:example-datastandardswales-medicationlist-discharge}}
    </div>
    <div id="tabjson" class="tabcontent">
      {{json:example-datastandardswales-medicationlist-discharge}}
    </div>       
    <div id="tabnarrative" class="tabcontent">
      {{narrative:example-datastandardswales-medicationlist-discharge}}
    </div>  
  </div>
</div>