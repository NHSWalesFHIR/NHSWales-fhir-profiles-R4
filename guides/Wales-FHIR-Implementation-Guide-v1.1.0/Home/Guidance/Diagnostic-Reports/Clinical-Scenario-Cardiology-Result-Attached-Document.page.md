# {{page-title}}

## Overview
Departments that can send binary attachments within NHS Wales to the Welsh Results & Reporting Service system are:

- Blood Science
- Cardiology
- Endoscopy
- Genetics
- Haematology
- Histology
- Microbiology
- Neurophysiology
- Radiology
- Respiratory
- Urology

## Implementation Guidance
Please refer to the {{pagelink:DataStandardsWales-DiagnosticReport,text:Data Standards Wales DiagnosticReport Profile}} page for general guidance.

For DiagnosticReport results with Attached Documents in NHS Wales:

* The `DiagnosticReport.meta.profile` field **SHALL** be <u>https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-DiagnosticReport</u>
<br><br>
* The `DiagnosticReport.presentedForm` field **SHALL** be populated
    * The `DiagnosticReport.presentedForm.contentType` field **SHALL** be populated
    * The `DiagnosticReport.presentedForm.data` field **SHALL** be populated with base64 string representation of the document
    * The `DiagnosticReport.presentedForm.title` field **SHALL** be populated
<br><br>
## Scenario 1
- Status: Final
- Security Label: Normal
- Category: Cardiology
- Encounter: Emergency Admission
- Result: ECG

### Logical Model
The diagram below shows the typical relationship between NHS Wales DiagnosticReport and presentedForm .
<br>

{{render:Diagrams-LogicalModel-DiagnosticReport-ReportDocument.drawio}}

<br />

### Example Result
Click {{pagelink:Example-DataStandardsWales-DiagnosticReport-ECG, text: here}} for an Example of a Diagnostic Report returning a Cardiology ECG report as presentedForm.

## Scenario 2
- Status: Final
- Security Label: Normal
- Category: Cardiology
- Result: Stress Test

### Example Result
Click {{pagelink:Example-DataStandardsWales-DiagnosticReport-StressTest, text: here}} for an Example of a Diagnostic Report returning a Cardiology Stress Test report as presentedForm.