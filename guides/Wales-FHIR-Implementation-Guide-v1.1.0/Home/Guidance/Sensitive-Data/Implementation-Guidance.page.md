# {{page-title}}

This page sets out guidance for the use of security labels with DataStandardsWales profiles. It describes how the security labels connect to the relevant resources.

## Security Labels used
DataStandardsWales resources as described above will return one of the following codes from [v3-Confidentiality Codesystem](http://terminology.hl7.org/CodeSystem/v3-Confidentiality){_target="blank"}. This is mapped from underlying NHS Wales system data:

* N - Normal
* R - Restricted

## Unrecognised security label
In the case a Security label is not returned with the resource the confidentiality should be regarded as Normal.

## Obligations around security labels
There is an obligation on the consuming system for data received from DataStandardsWales resources to appropriately handle results based on the Security Label attached to that resource.

## Meta Content

The following are examples of a Diagnostic Report that contains normal and sensitive data:

<div class="tab-wrap">
  <ul class="tab-head">
    <li class="tablink tab-active" onclick="openCity(this,'tabsnap')" data-target="tabsnap">
      Normal
    </li>
    <li class="tablink" onclick="openCity(this,'tabdiff')" data-target="tabdiff">
      Restricted/Sensitive
    </li>
  </ul>
  <div class="tab-main">
    <div id="tabsnap" class="tabcontent active">   

    <DiagnosticReport
      xmlns="http://hl7.org/fhir">
      <id value="1000012" />
      <meta>
        <versionId value="1" />
        <profile value="https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-DiagnosticReport" />
        <security>
          <system value="http://terminology.hl7.org/CodeSystem/v3-Confidentiality" />
          <code value="N" />
          <display value="Normal" />
        </security>
      </meta>
    ...  [snip] ...
    </DiagnosticReport>

  </div>

  <div id="tabdiff" class="tabcontent">

    <DiagnosticReport
      xmlns="http://hl7.org/fhir">
      <id value="1000012" />
      <meta>
        <versionId value="1" />
        <profile value="https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-DiagnosticReport" />
        <security>
          <system value="http://terminology.hl7.org/CodeSystem/v3-Confidentiality" />
          <code value="R" />
          <display value="Restricted" />
        </security>
      </meta>
    ...  [snip] ...
    </DiagnosticReport>

  </div>
</div>

