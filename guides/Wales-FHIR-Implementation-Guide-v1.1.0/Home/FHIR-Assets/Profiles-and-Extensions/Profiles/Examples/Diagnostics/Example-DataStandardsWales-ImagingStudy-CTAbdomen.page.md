<div class="warning"><span class="ClinicalWarn"></span></div>

## Example Imaging Study - Radiology DICOM Endpoint

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
      {{tree:example-datastandardswales-imagingstudy-ctabdomen}}
    </div>
    <div id="tabtable" class="tabcontent">
      {{table:example-datastandardswales-imagingstudy-ctabdomen}}
    </div>       
    <div id="tabxml" class="tabcontent active">      
      {{xml:example-datastandardswales-imagingstudy-ctabdomen}}
    </div>
    <div id="tabjson" class="tabcontent">
      {{json:example-datastandardswales-imagingstudy-ctabdomen}}
    </div>       
    <div id="tabnarrative" class="tabcontent">
      {{narrative:example-datastandardswales-imagingstudy-ctabdomen}}
    </div>  
  </div>
</div>