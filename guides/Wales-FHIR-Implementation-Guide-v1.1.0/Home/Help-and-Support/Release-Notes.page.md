## {{page-title}}

This page describes the published versions of this implementation guide and differences between versions:

### v1.1.1 STU1
Package:
* {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions,text:Profiles}}:
    * Changes to Profiles
        * DataStandardsWales-Provenance   
            * Updated references to use Data Standards Wales profiles     
* {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions,text:Extensions}}:
    * Changes to Extensions
        * DataStandardsWales-DemographicsAsRecorded
            * Renamed the DOB extension to birtDate 
            * Updated the extension URL
            * Updated the items within the extension URLs
        * DataStandardsWales-CDRPatientRecordType
            * Updated the name of the extension
        * DataStandardsWales-CDRSourceTimestamp
            * Updated the name of the extension

Guide:
* Updated the contact email address on the {{pagelink:Home/Help-and-Support/Related-Pages.page.md,text:Help and Support-Related Pages}}


            
### v1.1.0 STU1

Package: 
* {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions,text:Profiles}}:
    * New Profiles
        * DataStandardsWales-Device
        * DataStandardsWales-Provenance        
    * Changes to Profiles    
        * DataStandardsWales-Patient
            * Added Extensions for:
                * DataStandardsWales-CDRPatientRecordType
                * DataStandardsWales-CDRSourceTimestamp
* {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions,text:Extensions}}:
    * New Extensions
        * DataStandardsWales-CDRPatientRecordType
        * DataStandardsWales-CDRSourceTimestamp
        * DataStandardsWales-DemographicsAsRecorded

* {{pagelink:Home/FHIR-Assets/Terminology,text:Value Sets}}:
    * New Value Sets
        * DataStandardsWales-ProvenanceActivity
        * DataStandardsWales-PatientRecordType

 * {{pagelink:Home/FHIR-Assets/Naming-Systems.page.md,text:Naming Systems}}:
    * Corrected oid references. Changed from 2.16.840.1.113883.2.1.8.1.5.nnn to 2.16.840.1.113883.2.1.8.1.3.nnn    

Guide:
* Updated relevant pages within the Guide to reflect changes outlined in Package.
* Updated {{pagelink:Home/Help-and-Support/Glossary.page.md,text:Glossary}}.
  
* Added definitions for Active, Draft and Experimental to {{pagelink:Home/Introduction/Profile-Descriptions,text:Introduction-Profile Descriptions}}
* Added a link for FHIR PSOM Wales Project Page to {{pagelink:Home/Help-and-Support/Related-Pages.page.md,text:Help and Support-Related Pages}}
* Updated [Wales FHIR Implementation Guide Version History](https://simplifier.net/guide/Wales-FHIR-Implementation-Guide-Version-History-v1.1.0/Home/Version-History.page.md?version=1.1.0) to include links to respective Release Notes.


### v1.0.1 STU1

Package: 
* Profiles:
    * DataStandardsWales-Practitioner
        * Quotes removed from sdsuserid
    * DataStandardsWales-Location
        * Cardinality changed from 1..1 to 0..1:
            * .address
            * .managingOrganization.identifier
    * DataStandardsWales-MedicationDispense
        * Cardinality changed from 1..1 to 0..1:
            * .authorizingPrescription
            * .authorizingPrescription.reference
            * .identifier
            * .performer
            * .location.display
            * .quantity.value
            * .quantity.unit
            * .quantity.system
            * .quantity.code
        * Must support added to:
            * .location
            * .receiver
            * .context              
    * DataStandardsWales-Observation
        * Cardinality changed from 1..1 to 0..1:
            * .partOf.identifier
    * DataStandardsWales-Observation-Lab Resource
        * Corrected spelling error
* Code Systems:
    * DataStandardsWales-GenderIdentity
        * Trailing space removed from display value
    * DataStandardsWales-Sex
        * Trailing space removed from display value
* Value Set: 
    * DataStandardsWales-GenderIdentity
        * Trailing space removed from display value
    * DataStandardsWales-Sex
        * Trailing space removed from display value
    * DataStandardsWales-Title
        * Code expansion format corrected
* Concept Maps:
    * DataStandardsWales-GenderIdentity-HL7AdministrativeGender Resource
        * Corrected spelling error
        * Changed the targetURI to correct valueset
    * DataStandardsWales-HL7AdministrativeGender-GenderIdentity Resource
        * Changed the targetURI to correct valueset
    * DataStandardsWales-MaritalStatus-UKCorePersonMaritalStatusCode Resource
        * Changed the targetURI to correct valueset
        * Leading space removed from target value
* Extension:
    * DataStandardsWales-MedicationCourseOfTherapyType
        * Change to correct valueset
* Naming Systems:
    * Velindre PAS namespace OID corrected
    * BCUHB Central PAS Identifier corrected inconsistency
* Examples:
    * Organization - Glangwili General Hospital 
        * Removed hospital classification extension
    * Organization - Neath - Port Talbot Hospital 
        * Removed hospital classification extension
* Fixed render issues in ConceptsMaps, CodeSystem, NamingSystem & ValueSet by using HL7 FHIR XML element order
* Spaces removed in NamingSystems name to conform to HL7 as name can be used as id

Guide:
* DataStandardsWales-MedicationDispense
    * Mandatory and Must Support Data Elements list updated to reflect changes made to the profile and correct previously omitted information:
        * Updated the must have list as per current profile settings
        * Updated the must support list as per current profile settings   

### v1.0.0 STU1

* Changes made following feedback from the publication of the pre-release

### v1.0.0 STU1 - pre release

* Changes made in response to the ballot feedback process

### v0.1.1 STU1 - for ballot

* Minor errata to fix asset rendering issues

### v0.1.0 STU1 - for ballot

* First pass review of profiles
* Medication Scenarios
* Improvements to navigation
* Fixed page links and spelling
* Removed duplicate guidance
* References to HL7 or UK Core guidance where necessary


### 0.0.5 - Discovery

Experimental medication profiles were added.


* Immunization
* MedicationAdministration


The following experimental profiles were amended.


* MedicationDispense
* MedicationRequest


### 0.0.4 - Discovery

Experimental medication profiles were added.


* MedicationRequest
* MedicationDispense

A profile can now be designated as "Experimental" to show publishing intent in the near future.

### 0.0.2 & 0.0.3 - Discovery

Various profile drafts and fixes have been added.

### 0.0.1 - Discovery
The initial draft of the Data Standards Wales FHIR Implementation Guide, and should be considered 'under construction'. It contains only the base FHIR 'people and places' administrative resources.

This version is not intended for use, but is published for early comment and feedback.

<div class="container">
    <div class="row">
        <div class="col-md-7 card">
            <h4><b><a href="https://simplifier.net/guide/wales-fhir-implementation-guide-version-history" alt="Wales FHIR Implementation GUide Version History" target="_blank">Wales FHIR Implementation Guide Version History</a></b></h4>
            <p>Detailed description of the implementation guide changes</p>
        </div>
    </div>
</div>