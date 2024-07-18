<div class="warning"><span class="ImplementWarn"></span></div>

## {{page-title}}
An extension to carry an indicator of the overall pattern of medication administration at the MedicationStatement level.

### Purpose
This extension extends the MedicationStatement resource to carry an indicator of the overall pattern of medication administration at the MedicationStatement level (e.g. repeat or acute). This provides addition context to a clinician reviewing a list of patient medications to determine the reason why a patient is taking  a medication. 

### Context of Use
This extension may be used on the following profile(s):
* MedicationStatement

### Formal Views of Extension Content
<div class="tab-wrap">
  <ul class="tab-head">
    <li class="tablink tab-active" onclick="openCity(this,'tabsnap')" data-target="tabsnap">
      Snapshot View
    </li>
    <li class="tablink" onclick="openCity(this,'tabeg')" data-target="tabeg">
      Example View
    </li>
  </ul>
  <div class="tab-main">
    <div id="tabsnap" class="tabcontent active">      
      {{tree:https://fhir.nhs.wales/StructureDefinition/Extension-DataStandardsWales-MedicationCourseOfTherapyType, snapshot}}
    </div>
    <div id="tabeg" class="tabcontent">
      <list>
         <li>{{pagelink:Example-DataStandardsWales-MedicationStatement-DurogesicDTrans-GP, text:Durogesic DTrans (repeat)}}</li>
        <li>{{pagelink:Example-DataStandardsWales-MedicationStatement-Amoxicillin-GP, text:Amoxicillin (acute)}}</li>
      </list>
    </div>
  </div>
</div>