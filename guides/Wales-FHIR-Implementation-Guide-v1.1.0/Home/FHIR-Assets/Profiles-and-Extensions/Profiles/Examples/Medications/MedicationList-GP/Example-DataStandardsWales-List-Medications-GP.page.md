<div class="warning"><span class="ClinicalWarn"></span></div>

## Example Medications List - GP Record

This examples medication list is provided as part of a patient journey scenario, which is described {{pagelink:Home/Guidance/Medications/Index.page.md, text:here}}. The list references the following example resources:
* Subject, source and context:
  * {{pagelink:Example-DataStandardsWales-Patient-PeterPiper, text:Patient - Peter Piper}}
* Medication statements:
  * {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/Examples/Medications/MedicationList-GP/Example-DataStandardsWales-MedicationStatement-Bendro.-GP.page.md, text:Bendroflumethiazide}}
  * {{pagelink:Example-DataStandardsWales-MedicationStatement-Amoxicillin-GP, text:Amoxicillin}}
  * {{pagelink:Example-DataStandardsWales-MedicationStatement-Atorvastatin-GP, text:Atorvastatin}}
  * {{pagelink:Example-DataStandardsWales-MedicationStatement-Bisoprolol-GP, text:Bisoprolol}}
  * {{pagelink:Example-DataStandardsWales-MedicationStatement-DurogesicDTrans-GP, text:Durogesic DTrans}}
  * {{pagelink:Example-DataStandardsWales-MedicationStatement-Hydrocortisone-GP, text:Hydrocortisone}}
  * {{pagelink:Example-DataStandardsWales-MedicationStatement-Latanoprost-GP, text:Latanoprost}}
  * {{pagelink:Example-DataStandardsWales-MedicationStatement-Nifedipress-GP, text:Nifedipress}}
  * {{pagelink:Example-DataStandardsWales-MedicationStatement-Ramipril-GP, text:Ramipril}}

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
      {{tree:Example-DataStandardsWales-List-Medications-GP}}
    </div>
    <div id="tabtable" class="tabcontent">
      {{table:Example-DataStandardsWales-List-Medications-GP}}
    </div>       
    <div id="tabxml" class="tabcontent active">      
      {{xml:Example-DataStandardsWales-List-Medications-GP}}
    </div>
    <div id="tabjson" class="tabcontent">
      {{json:Example-DataStandardsWales-List-Medications-GP}}
    </div>       
    <div id="tabnarrative" class="tabcontent">
      {{narrative:Example-DataStandardsWales-List-Medications-GP}}
    </div>  
  </div>
</div>