# {{page-title}}

## Overview
Pathology is the most prevalent of the results in the Welsh Results & Reporting Service. Pathology covers many departmental areas:

- Blood Sciences (BSC)
- Bio-Chemistry (CHM)
- Immunology (IMM)
- Microbiology (MIC)
- Histopathology (HIS)
- Haematology
- Screening
- Andrology

## Implementation Guidance
Please refer to the {{pagelink:DataStandardsWales-DiagnosticReport-Lab,text: Data Standards Wales DiagnosticReport for Laboratory Results}} Profile page for general guidance.

For Pathology results in NHS Wales:


* The `DiagnosticReport.meta.profile` field **SHALL** be <u>https://fhir.nhs.wales/StructureDefinition/DataStandardsWales-DiagnosticReport-Lab</u>
<br><br>
* The `DiagnosticReport.result` field **SHALL** be populated
    * This field will be populated with the **Observation Group** containing 1 or multiple ObservationResults as Members.
<br><br>


## Scenario 1: Single Panel
- Status: Final
- Security Label: Normal
- Category: Pathology
- Code: FBC
- Result: FBC (Full Blood Count)

### Logical Model
The diagram below shows the typical relationship between NHS Wales DiagnosticReport and Observations.
<br>

{{render:Diagrams-LogicalModel-DiagnosticReport-SinglePanel.drawio}}

<br />

<div class="warning"><b>Important:</b> Single panel approach for Laboratory DiagnosticReports needs review and approval.</div>

### Example Result
Click {{pagelink:Example-DataStandardsWales-DiagnosticReport-FBC, text: here}} for an Example of a Diagnostic Report returning Pathology single panel Full Blood Count Blood Sciences result.

## Scenario 2: Multiple Panel
- Status: Final
- Security Label: Normal
- Category: Pathology
- Code: Pathology
- Results: ACE (Angiotensin Converting Enzyme), LFT (Liver Function Test)

### Logical Model
The diagram below shows the typical relationship between NHS Wales DiagnosticReport and Observations.
<br>

{{render:d-logicalmodel-diagnosticreport-multiplepanel-ureaelectrolytes.drawio}}

<br />
Click {{pagelink:Example-DataStandardsWales-DiagnosticReport-MultiplePanel, text: here}} for an Example of a Diagnostic Report returning Pathology multiple panel Blood Sciences result.
