## {{page-title}}

Some file names may become very long depending on the information they are trying to convey.  Asset identifiers generally inherit these names and may become invalid if they are over 64 characters, are not alpha numeric, or contain special characters (excluding -). File paths over 260 characters for certain windows systems will also cause problems due to operating system limits. Due to the above the file name and identifiers may have to diverge. The resources impacted the most are examples due to the increased amount of information they're attempting to convey.

The following considerations should be made to prevent this:

* Only alphanumeric characters and some special characters (recommend only hyphens -) should be use in file names and identifiers
* Ensure nested folder names use minimal characters
* Do not nest folders beyond a reasonable amount
* Keep full file paths well below 260 characters
* Try to keep the file name to the lowest amount of characters while maintaining context
* The file name may be longer and provide more context than the identifier.
* Use NHS Wales standard abbreviations where possible (e.g. ABUHB or PAS)
* If the name/identifier can be conveyed in under 64 characters then do not use any abbreviation
* If the name/identifier would be over 64 characters then:
    * Abbreviate some of the terms in the end of the file (e.g. full blood count becomes FBC)
    * If that is not enough, abbreviate DataStandardsWales to DSW in order to not completely lose the context in the full name
    * If this does not resolve the issue then the identifier/name should be reconsidered