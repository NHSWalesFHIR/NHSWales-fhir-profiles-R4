## {{page-title}}

### Release Strategy

We have recently moved from Discovery phase to a Standard for Trial Use 1 (STU1) for ballot as part of our release strategy.  The profiles in DRAFT have had a first pass review by our Interoperability Task & Finish Group to integrate coding standards and Value Sets as dictated by Data Standards Wales.

1. Discovery phase - completed
2. v0.1.1 STU1 for ballot - completed
3. v1.0.0 STU1 for pre-release - completed
4. v1.0.0 STU1 for implementation - published

This release strategy follows the [UK Core Publication History](https://simplifier.net/guide/ukcoreversionhistory?version=current).

### Balloting

Following the first STU1 for ballot release,  we will develop a review strategy to obtain feedback on profiles. This will be circulated in due course.

### Change Management

We are currently developing our change management strategy and we will ensure that all stakeholders are informed of changes to the implementation guide. To date this has been handled through the Interoperability Standards Working Group and the ballot process.  We have begun to use Azure DevOps to track all changes on a per release basis and we eventually turn the projects user stories into release notes.  These will be disseminated via an email distribution list which you can ask to be added to via the {{pagelink:Home/Help-and-Support/Help-and-Support.page.md,text:data standards email inbox}}. A more detailed breakdown of changes that have occurred in new releases will also be provided on the implementation guide.

### Standard for Trial Use (STU) Explanation

The STU nomenclature is used as standard terminology in FHIR implementation guides.  STU is usually suffixed with a number to denote the current version (e.g. STU1, STU2, etc...) and the number will increase after every ballot.  Due to this we have decided to adopted this naming convention for our releases.
<br>
It should be noted that HL7 and UK Core, who provide the base profiles our project uses, both have their own STU numbering. These and our own releases, therefore, have three separate STU numbering sequences that are not interchangeable.  Please ensure that the correct STU sequence is being referenced depending on the release and provider.

### Profile Status

The FHIR assets included in this guide can have a status of active or draft and can be flagged as experimental:

* Active - ready for use in implementation, full review has taken place
* Draft - proposed structure thay may become active in later releases, minimal review has taken place, should not be used for implementation
* Experimental - has not undergone any review, should not be used for implementtion, purely illustrative only

A mixture of active and draft FHIR resources are included in this guide and these have been published following the ballot feedback process. Some profiles are provided in a draft and/or experimental state and have not undergone a thorough review cycle.

### Profile Maturity

Active profiles can be used for implementation and we would encourage anyone beginning development to inform the InterOp Delivery Team so that assistance can be provided. This will also be used as an opportunity to review and influence the content in the implementation guide.

Active profiles have been scrutinised by the InterOp FHIR Task & Finish group and ballot process. While the profiles are designed to have some rigidity, the intention is for development to be flexible to the needs of system owners throughout NHS Wales. Development of these assets will continue in future iterations and as they increase in maturity the number of expected changes will decrease.

Draft and/or experimental assets may change regularly and should not be expected to remain more stable until an active version is published. It is recommended that implementors looking to utilise these profiles should only do so for testing purposes. Individuals are encouraged to engage in the development of these profiles to ensure they are fit for purpose. The inclusion of a draft or experimental asset does not guarantee it will become active in a future release and, while unlikely, they may be removed following consultation with key stakeholders.

