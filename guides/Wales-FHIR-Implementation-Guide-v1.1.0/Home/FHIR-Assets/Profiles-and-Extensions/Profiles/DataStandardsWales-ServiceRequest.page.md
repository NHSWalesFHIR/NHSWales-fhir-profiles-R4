<div class="warning"><span class="ExperiWarn"></span></div>

## {{page-title}}
The [ServiceRequest](https://www.hl7.org/fhir/r4/ServiceRequest.html) resource contains information of a request for a procedure or diagnostic or other service to be planned, proposed, or performed, as distinguished by the ServiceRequest.intent field value, with or on a patient.

The {{page-title}} profile is derived from the [UK Core STU2 ServiceRequest Profile](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-ServiceRequest?version=current) and is therefore listed as experimental. It defines additional rules for use within health and care organisations in Wales.

A direct link to the Data Standards Wales asset can be accessed here - {{link:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-ServiceRequest}}

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
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-ServiceRequest, snapshot}}
    </div>
    <div id="tabdiff" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-ServiceRequest, diff}}
  </div>
    <div id="tabhybrid" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-ServiceRequest, hybrid}}
  </div>
  <div id="tabeg" class="tabcontent">
    <list>
      <li>{{pagelink:Example-DataStandardsWales-ServiceRequest-PathologyOrder, text:Example ServiceRequest}}</li>
    </list>
  </div>    
</div>

## Implementation Guidance
This profile aligns with the [UK Core STU2 Service Request Profile](https://simplifier.net/guide/uk-core-implementation-guide-stu2/Home/ProfilesandExtensions/Profile-UKCore-ServiceRequest?version=current).


### Mandatory and Must Support Data Elements
Refer to the {{pagelink:Home/Introduction/Profile-Descriptions/Mandatory-and-Must-Support-Data-Elements.page.md,text: Mandatory and Must Support}} page for guidance on how these elements should be interpreted.
 
**Each Service Request must have:**
1. A status
1. An intent code indicating whether the request is a proposal, plan, or order.
1. A code defining what is being requested
1. A patient

**Each Service Request must support:**
1. An identifier *
1. A category
1. A priority
1. A reference to one or more specimens
1. When request was made
1. The requester

*see Implementation Guidance for the identifier element below


The `ServiceRequest.identifier` field **SHOULD** contain all available identifiers. Typical identifiers include:
  * Identifiers assigned to the ServiceRequest by the Welsh Results and Reporting Service
<br><br>

