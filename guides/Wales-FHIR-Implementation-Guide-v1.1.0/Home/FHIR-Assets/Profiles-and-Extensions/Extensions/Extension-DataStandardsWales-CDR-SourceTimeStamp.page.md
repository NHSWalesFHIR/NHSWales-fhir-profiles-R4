<div class="warning"><span class="ImplementWarn"></span></div>

## {{page-title}}
An extension to carry a timestamp for when a record has been updated.

### Purpose
This extension is intended for use within the Care Data Repository, and extends the Patient resource to record a timestamp that shows when the demographic record was last updated at source. This timestamp is used in the management of patient demographics and identity within the Care Data Repository.

### Context of Use
This extension may be used on the following profile(s):
* Patient

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
      {{tree:extensiondatastandardswalesCDRSourceTimestamp, snapshot}}
    </div>
    <div id="tabeg" class="tabcontent">
      <list>
         <li>Currently under development</li>
      </list>
    </div>
  </div>
</div>