## Overview
Radiology Imaging results can include the following types

- X-Rays
- Computed Tomography (CT)
- Magnetic Resonance Tomography (MRI)
- Nuclear Medicine Positron Emission Tomography (PET)
- Ultrasound

## Implementation Guidance
Please refer to the {{pagelink:DataStandardsWales-DiagnosticReport,text:Data Standards Wales DiagnosticReport Profile}} page for general guidance.

For Radiology Imaging results in NHS Wales:

* The `DiagnosticReport.meta.profile` field **SHALL** be <u>https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-DiagnosticReport</u>
<br><br>
* The `DiagnosticReport.imagingStudy` field **SHALL** be populated
<br><br>

## Scenario
- Status: Final
- Security Label: Normal
- Category: Radiology
- Code: CT Abdomen


### Logical Model
The diagram below shows the typical relationship between NHS Wales DiagnosticReport and Imaging .
<br>

{{render:Diagrams-LogicalModel-DiagnosticReport-ImagingStudy.drawio}}

<br />

### Example Results
 - Click {{pagelink:Example-DataStandardsWales-DiagnosticReport-CTAbdomen, text: here}} for an example of a Diagnostic Report returning a CT Abdomen ImagingStudy reference.
 - Click {{pagelink:Example-DataStandardsWales-ImagingStudy-CTAbdomen, text: here}} for an example of the referenced ImagingStudy.
 - Click {{pagelink:Example-DataStandardsWales-Endpoint-Dicom, text: here}} for an example of the referenced FHIR Endpoint.
