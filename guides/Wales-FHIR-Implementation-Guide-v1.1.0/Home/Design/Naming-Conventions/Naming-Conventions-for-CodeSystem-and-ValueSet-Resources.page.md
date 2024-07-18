### {{page-title}}
The following naming convention applies to FHIR CodeSystem and ValueSet resources:

The **logical id** of the resource shall be in the form **DataStandardsWales-[BusinessName]** e.g.
* DataStandardsWales-Sex
* DataStandardsWales-Title

The **URL** of the resource shall be in the form
**[base URL]/[ResourceType]/DataStandardsWales-[BusinessName]** e.g. 
* ```https://fhir.nhs.wales/CodeSystem/DataStandardsWales-Sex```
* ```https://fhir.nhs.wales/ValueSet/DataStandardsWales-Title```

The **name** of the resource - specifically the name.value.element - shall be in the form **DataStandardsWales[BusinessName]** e.g. 
* DataStandardsWalesSex
* DataStandardsWalesTitle

The **title** of the resource shall follow the name.value.element, using title case e.g.
* Data Standards Wales Sex
* Data Standards Wales Title

The **filename** of the resource shall be in the form **[ResourceType]-DataStandardsWales-[BusinessName]** e.g. 
* CodeSystem-DataStandardsWales-Sex
* ValueSet-DataStandardsWales-Title

<br>