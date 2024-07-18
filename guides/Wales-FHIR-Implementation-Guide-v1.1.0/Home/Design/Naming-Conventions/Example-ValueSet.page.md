### {{page-title}}
A fully populated ValueSet example is provided below to demonstrate the naming convention in use:

<div class="tab-wrap">
  <ul class="tab-head">
    <li class="tablink tab-active" onclick="openCity(this,'tabXML')" data-target="tabXML">
      XML View
    </li>
    <li class="tablink" onclick="openCity(this,'tabJSON')" data-target="tabJSON">
      JSON View
    </li>    
  </ul>
  <div class="tab-main">
    <div id="tabXML" class="tabcontent active">      
        {{xml:https://fhir.nhs.wales/ValueSet/DataStandardsWales-Title}}
    </div>
    <div id="tabJSON" class="tabcontent">
        {{json:https://fhir.nhs.wales/ValueSet/DataStandardsWales-Title}}
  </div>  
</div>