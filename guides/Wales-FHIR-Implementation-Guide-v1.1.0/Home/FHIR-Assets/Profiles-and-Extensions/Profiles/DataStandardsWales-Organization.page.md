<div class="warning"><span class="ImplementWarn"></span></div>

## {{page-title}}

### Overview

The [Organization](https://www.hl7.org/fhir/r4/organization.html) resource contains information about health and care organisations. Examples include Health Boards and NHS Trusts, Hospitals, Dental practices GP practices and GP clusters.  The {{page-title}} profile is derived from the [UK Core Organization Profile](https://simplifier.net/guide/uk-core-implementation-guide/Home/ProfilesandExtensions/ProfileUKCore-Organization?version=1.0.0). It defines additional rules for use within health and care organisations in Wales. Further guidance on the use of the Organization resource along with other administrative FHIR resources is provided within the {{pagelink:Home/Guidance/Administrative-Data, text: guidance}} section of this guide.

A direct link to the Data Standards Wales asset can be accessed here - {{link:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Organization}}

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
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Organization, snapshot}}
    </div>
    <div id="tabdiff" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Organization, diff}}
  </div>
    <div id="tabhybrid" class="tabcontent">
      {{tree:https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-Organization, hybrid}}
  </div>
  <div id="tabeg" class="tabcontent">
    <list>
      <li>{{pagelink:Example-DataStandardsWales-Organization-GGH, text: Glangwili General Hospital}}</li>
      <li>{{pagelink:Example-DataStandardsWales-Organization-NPT, text: Neath Port Talbot Hospital}}</li>
      <li>{{pagelink:Example-DataStandardsWales-Organization-HDUHB, text: Hywel Dda University Local Health Board}}</li>
      <li>{{pagelink:Example-DataStandardsWales-Organization-SBUHB, text: Swansea Bay University Local Health Board}}</li>
      <li>{{pagelink:Example-DataStandardsWales-Organization-GPPractice, text: GP Practice example}}</li>
      <li>{{pagelink:Example-DataStandardsWales-Organization-GPCluster, text: GP Cluster example}}</li>
    </list>
  </div>
</div>

### Mandatory and Must Support Data Elements
Refer to the {{pagelink:Home/Introduction/Profile-Descriptions/Mandatory-and-Must-Support-Data-Elements.page.md,text: Mandatory and Must Support}} page for guidance on how these elements should be interpreted.

Each Organisation must have:
* A name
  * The `Organization.name` field **SHALL** be populated.

Each Organisation must support:
* An identifier *
  * The `Organization.identifier` field **SHOULD** contain all available identifiers. Typical identifiers include:
    * The [Organisation Data Service](https://digital.nhs.uk/services/organisation-data-service) (ODS) issues and manages unique identification codes and accompanying reference data for organisations that interact with any area of the NHS. The ODS code for organisations managed by this service should be populated (this includes ANANA format codes).
    * A GP Cluster code for Welsh GP cluster organisations.

* A status of the organisation (i.e., whether is still active )
  * The `Organization.status` field **SHOULD** be populated to indicate whether the organisation is still active.

_*see Implementation Guidance for the identifier element below_

### Extensions

* The following extensions are defined for use within this profile: 
  * The UK Core extension [Extension-UKCore-MainLocation](https://simplifier.net/guide/uk-core-implementation-guide/Home/ProfilesandExtensions/ExtensionLibrary?version=1.0.0#ExtensionUKCore-MainLocation) extends the Organisation resource to support the exchange of information on the Organisation's main location, as a reference to a Location resource, which is currently not supported by the FHIR standard.
  * The HL7 common extension [organization-period](http://hl7.org/fhir/R4/extension-organization-period.html) describes the date range that the organisation should be considered available.
  


### Slices
The following identifier slices for use with the Organization profile are listed below. ODS Organisation Code is further described [UK Core Naming System](https://simplifier.net/guide/UKNamingSystems/Home?version=current) and GP Cluster code is further described in the [NHS Wales Data Dictionary](https://www.datadictionary.wales.nhs.uk/#!WordDocuments/corereferencedatastandards1.htm).
 
* `Organization.identifier:odsOrganisationCode` 
* `Organization.identifier:gpClusterCode` 
 


