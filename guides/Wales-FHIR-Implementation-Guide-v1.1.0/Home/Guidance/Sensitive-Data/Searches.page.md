# {{page-title}}

It **SHOULD** be possible to limit search results based on their confidentiality by using the querystring **_tag={CodeSystem|Code}**. Some examples include:

## Sensitive/Restricted
A client interested in all sensitive data by Patient and Code can use the following query:

```
GET [base]/[resource]?patient=[id]&code=[code]&_tag=http://terminology.hl7.org/CodeSystem/v3-Confidentiality|R
```

## Non-Sensitive/Not Restricted
A client requesting non-sensitive data can either, not include the Tag as per the example below:
```
GET [base]/[resource]?patient=[id]&code=[code]
```
or may decide to include the _tag with a confidentiality of N
```
GET [base]/[resource]?patient=[id]&code=[code]&_tag=http://terminology.hl7.org/CodeSystem/v3-Confidentiality|N
```

## UK Core Access
Please also refer to {{pagelink:Home/Design/UK-Core-Access.page.md,text:UK Core Access}} for further details on standardising clinical data queries.

