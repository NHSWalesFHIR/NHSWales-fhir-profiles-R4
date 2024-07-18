<div class="warning"><span class="ClinicalWarn"></span></div>

## Example Medications List - Medicines on admission

This examples medication list is provided as part of a patient journey scenario, which is described {{pagelink:Home/Guidance/Medications/Index.page.md, text:here}}. The list references the following example resources:
* Subject, source and context:
  * {{pagelink:Example-DataStandardsWales-Patient-PeterPiper, text:Patient - Peter Piper}}
* Medication statements:
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-GP/Example-DataStandardsWales-MedicationStatement-Bendro.-GP.page.md, text:Bendroflumethiazide}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-GP/Example-DataStandardsWales-MedicationStatement-Bisoprolol-GP.page.md, text:Bisoprolol}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-GP/Example-DataStandardsWales-MedicationStatement-Nifedipress-GP.page.md, text:Nifedipress}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-GP/Example-DataStandardsWales-MedicationStatement-Ramipril-GP.page.md, text:Ramipril}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-GP/Example-DataStandardsWales-MedicationStatement-Atorvastatin-GP.page.md, text:Atorvastatin}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-GP/Example-DataStandardsWales-MedicationStatement-DurogesicDTrans-GP.page.md, text:Durogesic DTrans}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-GP/Example-DataStandardsWales-MedicationStatement-Hydrocortisone-GP.page.md, text:Hydrocortisone}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-GP/Example-DataStandardsWales-MedicationStatement-Latanoprost-GP.page.md, text:Latanoprost}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-GP/Example-DataStandardsWales-MedicationStatement-Amoxicillin-GP.page.md, text:Amoxicillin}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Outpatient/Example-DataStandardsWales-MedicationStatement-Enbrel-Outpatient.page.md, text:Enbrel}}
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Admission/Example-DataStandardsWales-MedicationStatement-Parace.-Admission.page.md, text:Paracetamol}}  
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-Admission/Example-DataStandardsWales-MedicationStatement-Ibupro.-Admission.page.md, text:Ibuprofen}}

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
      {{tree:Example-MedicationList-Admission}}
    </div>
    <div id="tabtable" class="tabcontent">
      {{table:Example-MedicationList-Admission}}
    </div>       
    <div id="tabxml" class="tabcontent active">      
      {{xml:Example-MedicationList-Admission}}
    </div>
    <div id="tabjson" class="tabcontent">
      {{json:Example-MedicationList-Admission}}
    </div>       
    <div id="tabnarrative" class="tabcontent">
      {{narrative:Example-MedicationList-Admission}}
    </div>  
  </div>
</div>