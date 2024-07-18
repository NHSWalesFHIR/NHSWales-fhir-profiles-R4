---
igversion: 1.1.0
---

# Wales FHIR Implementation Guide v{{variable: igversion}} STU1 <a class="btn btn-primary justify-content-md-center" href="#resourceindex" role="button" background-color="21305f">Scroll to resource index</a>

<div class="warning"><b>Important:</b> This is the v{{variable: igversion}} Standard for Trial use (STU1) release of the Data Standards Wales FHIR Implementation Guide. Please be aware that these pages refer to a mixture of active/draft/experimental assets as well as clinical scenarios that are undergoing review.</div>



## Project Description and Scope

<div class="container-fluid">
<div class="row">
	<div class="col">
This Implementation Guide contains the HL7 FHIR R4 standards for use by Health and Care organisations in Wales. The Data Standard Wales profiles have been developed with NHS Wales systems in mind and are derived from the UK Core STU1 v1.0.0 release. All relevant NHS Wales Data Standards have been implemented as appropriate.
<br></br>
These pages contain guidance on the following areas:
<br></br>

<ul class="list-group">
<li>FHIR resource profiles and extensions</li>
<li>FHIR terminology components including ValueSets, CodeSystems and ConceptMaps</li>
<li>Example FHIR resources</li>
<li>Other general guidance useful to FHIR implementers in Wales</li>
</ul>

</div>
	<div class="col">
			<div class="col-md-7 card text-center ">
  <div class="card-body">
    <h4 class="card-title"><b>{{pagelink:Home/Help-and-Support/Related-Pages.page.md,text: Related Pages}}</b></h4>
    <p class="card-text">Links related to NHS Wales FHIR development and UK Core</p>
	</div>
	</div>
			<div class="col-md-7 card text-center">
  <div class="card-body">
    <h4 class="card-title"><b>{{pagelink:Home/Help-and-Support/Version-Control-and-Ballot-Process.page.md}}</b></h4>
    <p class="card-text">Outline of how active, draft, and experimental resources should be handled by implementers</p>
				</div>
				</div>
				<div class="col-md-7 card text-center">
				  <div class="card-body">
    <h4 class="card-title"><b>{{pagelink:Home/Help-and-Support/Help-and-Support.page.md,text: Help and Support}}</b></h4>
    <p class="card-text">For suggestions or queries, please email Data Standards Wales using the link on this page</p>
		</div>
			</div>
			</div>
		</div>
	</div>

### Resource Index <a id="resourceindex"></a>

<table class="table table-striped">
  <thead>
    <tr>
      <th scope="col">People</th>
      <th scope="col">Entities</th>
      <th scope="col">Workflow</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td scope="row">{{pagelink:DataStandardsWales-Patient}} <a href="/ui/workflow/overview?id=1" class="tagactive" target="_blank">Active</a></td>
      <td>{{pagelink:DataStandardsWales-Location}} <a href="/ui/workflow/overview?id=1" class="tagactive" target="_blank">Active</a></td>	 
      <td>{{pagelink:DataStandardsWales-Encounter}} <a href="/ui/workflow/overview?id=1" class="tagdraft" target="_blank">Draft</a><div class="tagexperimental tt">E<span class="tooltiptext">Experimental profile</span></div></td>	  
    </tr>
    <tr>
      <td scope="row">{{pagelink:DataStandardsWales-Practitioner}} <a href="/ui/workflow/overview?id=1" class="tagactive" target="_blank">Active</a></td>
      <td>{{pagelink:DataStandardsWales-Organization}} <a href="/ui/workflow/overview?id=1" class="tagactive" target="_blank">Active</a></td>
    </tr>
    <tr>
	  <td scope="row">{{pagelink:DataStandardsWales-PractitionerRole}} <a href="/ui/workflow/overview?id=1" class="tagactive" target="_blank">Active</a></td>
    </tr>
  </tbody>
</table>


<table class="table table-striped">
  <thead>
    <tr>
      <th scope="col">Diagnostics</th>
      <th scope="col">Medication</th>
      <th scope="col">Allergy</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td scope="row">{{pagelink:DataStandardsWales-ServiceRequest}} <a href="/ui/workflow/overview?id=1" class="tagdraft" target="_blank">Draft</a><div class="tagexperimental tt">E<span class="tooltiptext">Experimental profile</span></td>
      <td>{{pagelink:DataStandardsWales-Medication}} <a href="/ui/workflow/overview?id=1" class="tagactive" target="_blank">Active</a></td>
      <td>{{pagelink:DataStandardsWales-AllergyIntolerance}} <a href="/ui/workflow/overview?id=1" class="tagactive" target="_blank">Active</a></td>
	</tr>
	<tr>
	  <td scope="row">{{pagelink:DataStandardsWales-DiagnosticReport}}  <a href="/ui/workflow/overview?id=1" class="tagdraft" target="_blank">Draft</a><div class="tagexperimental tt">E<span class="tooltiptext">Experimental profile</span></td>
      <td>{{pagelink:DataStandardsWales-MedicationAdministration}} <a href="/ui/workflow/overview?id=1" class="tagactive" target="_blank">Active</a></td>
	  <td>{{pagelink:DataStandardsWales-AllergyList}} <a href="/ui/workflow/overview?id=1" class="tagactive" target="_blank">Active</a></td>
	</tr>
	<tr>
	  <td scope="row">{{pagelink:DataStandardsWales-DiagnosticReport-Lab}}  <a href="/ui/workflow/overview?id=1" class="tagdraft" target="_blank">Draft</a><div class="tagexperimental tt">E<span class="tooltiptext">Experimental profile</span></td>
	  <td>{{pagelink:DataStandardsWales-MedicationDispense}} <a href="/ui/workflow/overview?id=1" class="tagactive" target="_blank">Active</a></td>
	</tr>
	<tr>
	  <td scope="row">{{pagelink:DataStandardsWales-Observation}}  <a href="/ui/workflow/overview?id=1" class="tagdraft" target="_blank">Draft</a><div class="tagexperimental tt">E<span class="tooltiptext">Experimental profile</span></td>
	  <td>{{pagelink:DataStandardsWales-MedicationList}} <a href="/ui/workflow/overview?id=1" class="tagactive" target="_blank">Active</a></td>
	</tr>
	<tr>
	  <td scope="row">{{pagelink:DataStandardsWales-Observation-Lab}}  <a href="/ui/workflow/overview?id=1" class="tagdraft" target="_blank">Draft</a><div class="tagexperimental tt">E<span class="tooltiptext">Experimental profile</span></td>
	  <td>{{pagelink:DataStandardsWales-MedicationRequest}} <a href="/ui/workflow/overview?id=1" class="tagactive" target="_blank">Active</a></td>
	</tr>
	<tr>
	  <td scope="row">{{pagelink:DataStandardsWales-Specimen}}  <a href="/ui/workflow/overview?id=1" class="tagdraft" target="_blank">Draft</a><div class="tagexperimental tt">E<span class="tooltiptext">Experimental profile</span></td>
	  <td>{{pagelink:DataStandardsWales-MedicationStatement}} <a href="/ui/workflow/overview?id=1" class="tagactive" target="_blank">Active</a></td>
	</tr>
	<tr>
	  <td scope="row">{{pagelink:DataStandardsWales-ImagingStudy}}  <a href="/ui/workflow/overview?id=1" class="tagdraft" target="_blank">Draft</a><div class="tagexperimental tt">E<span class="tooltiptext">Experimental profile</span></td>
	  <td>{{pagelink:DataStandardsWales-Dosage}}  <a href="/ui/workflow/overview?id=1" class="tagdraft" target="_blank">Draft</a><div class="tagexperimental tt">E<span class="tooltiptext">Experimental profile</span></div></td>
	</tr>
	<tr>
	  <td scope="row">{{pagelink:DataStandardsWales-Endpoint}}  <a href="/ui/workflow/overview?id=1" class="tagdraft" target="_blank">Draft</a><div class="tagexperimental tt">E<span class="tooltiptext">Experimental profile</span></td>
	  <td>{{pagelink:DataStandardsWales-Immunization}}  <a href="/ui/workflow/overview?id=1" class="tagdraft" target="_blank">Draft</a><div class="tagexperimental tt">E<span class="tooltiptext">Experimental profile</span></td>
	</tr>
	<tr>
		<td scope="row">{{pagelink:DataStandardsWales-Device}}  <a href="/ui/workflow/overview?id=1" class="tagdraft" target="_blank">Draft</a><div class="tagexperimental tt">E<span class="tooltiptext">Experimental profile</span></td>
    </tr>
  </tbody>
</table>

<table class="table table-striped" style="width:33%">
  <thead>
    <tr>
      <th scope="col">Security and Privacy</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td scope="row">{{pagelink:DataStandardsWales-Provenance}} <a href="/ui/workflow/overview?id=1" class="tagdraft" target="_blank">Draft</a><div class="tagexperimental tt">E<span class="tooltiptext">Experimental profile</span></td>
    </tr>
  </tbody>
</table>
