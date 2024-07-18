## {{page-title}}
This implementation guide include the following resources for allergy.
* {{pagelink:DataStandardsWales-AllergyList}}
* {{pagelink:Home/FHIR-Assets/Profiles-and-Extensions/Profiles/DataStandardsWales-AllergyIntolerance.page.md}}

### Clinical scenario: producing an Allergy List  
In this scenario, a patient is admitted as an inpatient; allergies are made available from several sources in varying quality. The end user will need to refine this prior to prescribing.  The allergies are presented, checked and the current allergies list is created.  

The purpose of these examples is to illustrate FHIR usage based on a simple clinical scenario. 

#### 1) Prior to admission
If degraded allergies are recorded then steps will need to be taken during admission to make the record safe prior to treatment or prescription. The degraded allergies will need to be coded correctly and updated. No list exists at this stage and the query specified it should be returned if present.

##### All Allergy information available- no current list exists
* Potato
* Aspirin, Ibuprofen (transfer degraded) 
* Aspirin 
* Wasps (transfer degraded) 
* Morphine/oramorph (transfer degraded) 


#### 2) After admission
The allergy information has been refined by the user by consulting with the patient and finding equivalent coded substances and findings or disorders. Each allergy resource is updated as these changes occur. No current list need exist at this stage.

##### All Allergy information refined- items corrected
* Potato
* Ibuprofen 
* Aspirin 
* Wasp 
* Morphine

#### 3) On discharge or transfer
 After the visit, the patient's medications and allergies form a part of the discharge or transfer message. To encapsulate the current view at the point of discharge a current allergy list is generated and added to, or referenced by, outbound messaging.

##### Current Allergy list generated
* Potato
* Ibuprofen 
* Aspirin 
* Wasp 
* Morphine


### Clinical scenario: updating an Allergy List  
In this scenario, a patient is admitted as an inpatient; allergies are made available from an existing allergy list. The end user needs to update the list to add a newly discovered allergy and to update any existing items to make the list conformal.

#### 1) On admission
The user has been presented with a list of no known allergies, meaning it is understood the user has no allergies. 


#### 2) During admission
The patient informs the user that they recently had a reaction to strawberries. The user **must** soft delete the no known allergies entry, add the strawberry allergy and update the current list.


#### 3) On discharge or transfer
After the visit, the patient's medications and allergies form a part of the discharge or transfer message. To encapsulate the current view at the point of discharge the current allergy list is added to, or referenced by, outbound messaging.
