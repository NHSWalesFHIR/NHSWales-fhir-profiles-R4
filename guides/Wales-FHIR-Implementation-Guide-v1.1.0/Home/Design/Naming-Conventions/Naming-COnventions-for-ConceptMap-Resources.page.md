### {{page-title}}
The following naming convention applies to FHIR ConceptMap resources:

The **logical id** of the resource shall be in the form **DataStandardsWales-[BusinessNameValueSetSource]-[BusinessNameValueSetTarget]** e.g.
* DataStandardsWales-UKCoreBirthSex-Sex
* DataStandardsWales-GenderIdentity-HL7AdministrativeGender

The **URL** of the resource shall be in the form
**[base URL]/[ResourceType]/DataStandardsWales-[BusinessNameValueSetSource]-[BusinessNameValueSetTarget]** e.g. 
* ```https://fhir.nhs.wales/ConceptMap/DataStandardsWales-UKCoreBirthSex-Sex```
* ```https://fhir.nhs.wales/ConceptMap/DataStandardsWales-GenderIdentity-HL7AdministrativeGender```

The **name** of the resource - specifically the name.value.element - shall be in the form **DataStandardsWales-ConceptMap-[BusinessNameValueSetSource]-to-[BusinessNameValueSetTarget]** e.g. 
* DataStandardsWales-ConceptMap-UKCoreBirthSex-to-Sex
* DataStandardsWales-ConceptMap-GenderIdentity-to-HL7AdministrativeGender

The **title** of the resource - specifically the name.value.element - shall be in the form **Data Standards Wales Concept Map from [Business Name ValueSet Source] to [Business Name ValueSet Target]** e.g.
* Data Standards Wales Concept Map from UK Core Birth Sex to Sex
* Data Standards Wales Concept Map from Gender Identity to HL7 Administrative Gender

The **filename** of the resource shall be in the form **Data Standards Wales Concept Map from [Business Name ValueSet Source] to [Business Name ValueSet Target]** e.g. 
* ConceptMap-DataStandardsWales-UKCoreBirthSex-Sex
* ConceptMap-DataStandardsWales-GenderIdentity-HL7AdministrativeGender

<br>