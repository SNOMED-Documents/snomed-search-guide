# Appendix C- An Example Search and Data Entry Overview Table

This section presents an example of a table, which is currently under development, intended to provide an overview of the various search techniques presented in this document, and their applications.

## Search by Term Text – Overview Table

Table assumptions:

* Search terms are at least 3 characters (what about phrases like 'of' or very short terms like "mg" or "MI")
* Filters should be applied
* Case sensitivity
* Search term preparation (and maybe SNOMED CT term preparation)

Ordering and presentation have not been considered.

<table><thead><tr><th width="168.078125"></th><th width="237.91796875">Example search scenario</th><th width="183.953125" valign="middle">Environment ?- Very useful ? - not very useful</th><th></th><th>Potential Nuber of results</th><th>Implementation Complexity</th></tr></thead><tbody><tr><td></td><td></td><td valign="middle">Browser</td><td>Clinical</td><td></td><td></td></tr><tr><td>Exact phrase</td><td>When the user knows the exact term string that he requires</td><td valign="middle">?</td><td>?</td><td>Low</td><td>Simple</td></tr><tr><td>Search for descriptions that begin with the search text</td><td>User needs to find terms where they know the root of the word/words they are looking for but not the order that it might be in in a term string.</td><td valign="middle">?</td><td>?</td><td>Medium</td><td>Moderate</td></tr><tr><td>Search for descriptions that contain the search text</td><td>When the user somewhat knows the term string that they require but not the full description</td><td valign="middle">?</td><td>?</td><td>High</td><td>Simple</td></tr><tr><td>Search for descriptions that end with the search text</td><td>When the user may want to search for the required text at the end of words</td><td valign="middle">?</td><td>?</td><td>Low</td><td>Moderate</td></tr><tr><td>Search for words within a description in any order</td><td>When the user does not how words are ordered in the Descriptions.</td><td valign="middle">?</td><td>?</td><td>High</td><td>Moderate</td></tr><tr><td>Search for identical terms</td><td>When the user knows the exact term string that they require</td><td valign="middle">?</td><td>?</td><td>Low</td><td>Simple</td></tr><tr><td>Search for word(s) in a specific order (or a matching phrase)</td><td>When the user somewhat knows the term string that they require but not the full description</td><td valign="middle">?</td><td>?</td><td>Medium</td><td>Moderate</td></tr><tr><td>Search for Concept Identifiers</td><td>When the user wants to know the Description of the Concept that he requires</td><td valign="middle">?</td><td>?</td><td>Low</td><td>Simple</td></tr><tr><td>Search for Description Identifiers</td><td>When the user wants to knows the Concept of the Description that he requires</td><td valign="middle">?</td><td>?</td><td>Low</td><td>Simple</td></tr></tbody></table>

