### {{page-title}}

The naming conventions defined here use the following naming segments:

**[base URL]:** the base URL  is https://fhir.nhs.wales/

**[ResourceType]:** The FHIR resource type e.g. 'StructureDefinition', 'CodeSystem', 'ConceptMap', 'Patient', or 'MedicationStatement'.  

**[BusinessName]:** The business name of the resource. For CodeSystem and ValueSet, the business name shall reflect the name given to the data set as published in the relevant Data Standards Change Notice (DSCN). For ConceptMap resources, the business name shall reflect the name given to the value set that is being mapped from. 

**[Organisation]:** NamingSystem resources may be 'owned' by a particular organisation. In this case use initials e.g. ABUHB (Aneurin Bevan University Health Board), VUNHST (Velindre Univerisity NHS Trust) etc. to identify the organisation.

<!--
*Note that in some cases the HL7 FHIR standard mandates value sets that do not match the equivalent Wales data standards e.g. [AdministrativeGender](https://hl7.org/fhir/R4/valueset-administrative-gender.html). In this case a concept map is required to map from the HL7 standard to the Welsh standard.*
-->
<br>