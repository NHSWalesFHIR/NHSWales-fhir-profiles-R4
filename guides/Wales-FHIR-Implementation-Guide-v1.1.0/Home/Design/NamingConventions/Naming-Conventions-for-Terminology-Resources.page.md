### {{page-title}}
The following naming convention applies to FHIR CodeSystem, ConceptMap and ValueSet resources:

The **logical id** of the CodeSystem shall be in the form **DataStandardsWales-[BusinessName]** e.g.
* DataStandardsWales-Ethnicity,
* DataStandardsWales-MaritalStatus

The **URL** of the resource shall be in the form
**[base URL]/[ResourceType]/DataStandardsWales-[BusinessName]** e.g. 
* https&#58;//fhir.nhs.wales/CodeSystem/DataStandardsWales-Ethnicity
* https&#58;//fhir.nhs.wales/ValueSet/DataStandardsWales-GenderIdentity
* https&#58;//fhir.nhs.wales/ConceptMap/DataStandardsWales-AdministrativeGender

<!--
<html>
    <div class="warning-red"><b>Issue:</b> The convention above for resource.id is problematic - must prefix with  [ResourceType] to ensure resource identities are unique on Simplifier. To be discussed at the Wales Interoperabilty Group on 17/06/2021.</div><br>
</html>
-->

The **name** of the resource - specifically the name.value.element - shall be in the form **DataStandardsWales[BusinessName]** e.g. 
* DataStandardsWalesEthnicity
* DataStandardsWalesMaritalStatus

The **title** of the resource shall follow the name.value.element, using title case e.g.
* Data Standards Wales Ethnicity
* Data Standards Wales Marital Status

The **filename** of the resource shall be in the form **[ResourceType]-DataStandardsWales-[BusinessName]** e.g. 
* CodeSystem-DataStandardsWales-Ethnicity
* ConceptMap-DataStandardsWales-AdministrativeGender

<br>