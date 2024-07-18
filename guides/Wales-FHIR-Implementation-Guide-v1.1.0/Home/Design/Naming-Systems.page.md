<div class="warning"><span class="ImplementWarn"></span></div>

## {{page-title}}

### System Identifier Namespaces for Welsh Patient Identifiers
The diagram below shows the naming convention used for system identifier namespaces for Welsh Patient identifiers. 
{{render:images-systemidentifiernamespacesforwelshpatientidentifiers}}

The example above is based on the following principles:
* Follow the UK Core guidelines for naming systems where possible.
  * e.g. Manchester University NHS Foundation Trust - ```https://fhir.mft.nhs.uk/Id/pas-number```
  * e.g. Leeds City Council - ```https://fhir.leeds.gov.uk/Id/socialcare-number```
* The namespace* should include the domain of the organisation responsible for creating and maintaining the identifier.
  * e.g. ```https://fhir.abuhb.nhs.wales/Id/socialcare-number```
* Use URLs and not OIDs for key systems. 
  * While it is agreed that more meaningful URLs should be used in place of OIDs it is not practical to maintain namespaces for the 200+ systems currently that have an OID registered with the MPI. Therefore, system identifier namespaces shall only be created for the key systems which are likely to provide identifiers with relevance to other systems – such as a Health Board PAS identifiers. 
  * Other key systems to be agreed.
* The text ‘pas-identifier’ is used to identify a PAS patient identifier  

*Avoid use of alternatives such as ‘CRN’, ‘pas-number’, ‘pas-id’, ‘patient-identifier’ etc.

### Commonly Used Patient System Identifier Namespaces
The commonly used namespaces for PAS patient identifiers are available on the {{pagelink:Home/FHIR-Assets/Naming-Systems.page.md}} page.