## {{page-title}}

Sensitive records relate directly to data that is considered as highly confidential in nature. In NHS Wales systems, sensitive records (e.g. test results, clinical documents, medications) are flagged,  requiring the user to 'break glass' in order to view that record.

This page describes how the Data Standards Wales profiles can support flagging FHIR resources as having sensitive data via the information in the resource metadata tag.

This implementation guide references the following profiles that may contain sensitive data (this list is not exhaustive):

* {{pagelink:DataStandardsWales-DiagnosticReport}}
* {{pagelink:DatastandardsWales-Medication}}*
* {{pagelink:DataStandardsWales-Observation}}
* {{pagelink:DataStandardsWales-ServiceRequest}}

*all associated medication resources may contain sensitive data

## Profile metadata

Profiles can have metadata associated with them that are not listed in the core specification.  An overview of associated profile metadata can be found on the [HL7 FHIR R4 Resoure Definitions](http://hl7.org/fhir/R4/resource-definitions.html) page.

##	Meta.security and Meta.Tags

The metadata elements Meta.security and Meta.Tag may contain additional coding that can be used to drive security specific data retrieval.

## Security Labels

A [security label](http://hl7.org/fhir/R4/security-labels.html){_target=blank} is a concept attached to a resource or bundle that provides specific security metadata about the information it is fixed. The intent of a security label is that the recipient of resources or bundles with security labels is obligated to enforce any handling caveats and carry security restrictions forward as appropriate.