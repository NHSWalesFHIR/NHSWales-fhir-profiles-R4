<div class="warning"><span class="ClinicalWarn"></span></div>

## Example Medications List - Inpatient medication

This examples medication list is provided as part of a patient journey scenario, which is described {{pagelink:Home/Guidance/Medications/Index.page.md, text:here}}. The list references the following example resources:
* Subject, source and context:
  * {{pagelink:Example-DataStandardsWales-Patient-PeterPiper, text:Patient - Peter Piper}}
* Medication statements:
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Inpatient/Example-DataStandardsWales-MedicationStatement-Bendro.-Inpatient.page.md, text:Bendroflumethiazide}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Inpatient/Example-DataStandardsWales-MedicationStatement-Bisop.-Inpatient.page.md, text:Bisoprolol}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Inpatient/Example-DataStandardsWales-MedicationStatement-Nifedi.-Inpatient.page.md, text:Nifedipress}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Inpatient/Example-DataStandardsWales-MedicationStatement-Ramipr.-Inpatient.page.md, text:Ramipril}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Inpatient/Example-DataStandardsWales-MedicationStatement-Atorva.-Inpatient.page.md, text:Atorvastatin}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Inpatient/Example-DataStandardsWales-MedicationStatement-Parace.-Inpatient.page.md, text:Paracetamol}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Inpatient/Example-DataStandardsWales-MedicationStatement-Duroge.-Inpatient.page.md, text:Durogesic DTrans}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Inpatient/Example-DataStandardsWales-MedicationStatement-Hydroc.-Inpatient.page.md, text:Hydrocortisone}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Inpatient/Example-DataStandardsWales-MedicationStatement-Latano.-Inpatient.page.md, text:Latanoprost}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Inpatient/Example-DataStandardsWales-MedicationStatement-Enbrel-Inpatient.page.md, text:Enbrel}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Inpatient/Example-DataStandardsWales-MedicationStatement-Ibupro.-Inpatient.page.md, text:Ibuprofen (stopped)}}

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
      {{tree:example-datastandardswales-list-medications-inpatient}}
    </div>
    <div id="tabtable" class="tabcontent">
      {{table:example-datastandardswales-list-medications-inpatient}}
    </div>       
    <div id="tabxml" class="tabcontent active">      
      {{xml:example-datastandardswales-list-medications-inpatient}}
    </div>
    <div id="tabjson" class="tabcontent">
      {{json:example-datastandardswales-list-medications-inpatient}}
    </div>       
    <div id="tabnarrative" class="tabcontent">
      {{narrative:example-datastandardswales-list-medications-inpatient}}
    </div>  
  </div>
</div>