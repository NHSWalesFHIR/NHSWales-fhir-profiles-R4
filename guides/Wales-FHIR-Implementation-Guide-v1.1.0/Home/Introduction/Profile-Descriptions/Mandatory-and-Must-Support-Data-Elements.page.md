### {{page-title}}
Each profile description includes _Mandatory_ and _Must Support_ elements. 

### Mandatory

In order to be compliant, when an element is mandatory (min=1), the data is expected to always be present - i.e. **SHALL** be present. Figure 1 below shows how _Mandatory_ elements are presented in the Snapshot View. 
<br><br>
**Figure 1: Mandatory Elements**
{{render:Diagrams-Guidance-MandatoryElements}}
<br>

### Must Support

Elements marked with an <span style="background-color:red;color:white;">S</span> must be supported. While the definition of _Must Support_ is quite general, this implementation guide defines it to mean that provider **SHOULD** populate these elements where possible, and consumer systems **SHOULD** act on this information if provided.

If the data does not exist or it is currently technically impossible to populate a _Must Support_ element then you are _not_ required to populate the element. However, it would be expected that in future iterations the system does provide the necessary information.

Depending on the scenario certain _Must Support_ elements may **NOT** need to be populated. An example would be specialty, if a practitioner does not have one then it does not need to be populated but the element must be supported as other practitioners may have a specialty.

### Organization Example

In the case of the `Oganization.active` element, _Must Support_ would mean, for example:
* A provider system would be expected to provide the relevant indicator to show if the organisation is still active.
* A consuming  system would be expected to act on this information and not include an organisation marked as inactive within a list of active organisations.

Figure 2 below shows how _Must Support_ elements are presented in the Snapshot View. 
<br><br>
**Figure 2: Must Support Elements**
{{render:Diagrams-Guidance-MustSupportElements}}
<br>
