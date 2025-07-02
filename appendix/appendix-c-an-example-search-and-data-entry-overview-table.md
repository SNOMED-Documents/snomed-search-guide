# Appendix C- An Example Search and Data Entry Overview Table

This section presents an example of a table, which is currently under development, intended to provide an overview of the various search techniques presented in this document, and their applications.

## Search by Term Text – Overview Table

Table assumptions:

* Search terms are at least 3 characters (what about phrases like 'of' or very short terms like "mg" or "MI")
* Filters should be applied
* Case sensitivity
* Search term preparation (and maybe SNOMED CT term preparation)

Ordering and presentation have not been considered.

\| **Example search scenario**| **Environment**\
? - Very useful\
? - not very useful| | **Potential Number of results**| **ImplementationComplexity**\
\---|---|---|---|---|---\
\| | Browser| Clinical| |\
Exact phrase| When the user knows the exact term string that he requires| ?| ?| Low| Simple\
Search for descriptions that begin with the search text| User needs to find terms where they know the root of the word/words they are looking for but not the order that it might be in in a term string.| ?| ?| Medium| Moderate\
Search for descriptions that contain the search text| When the user somewhat knows the term string that they require but not the full description| ?| ?| High| Simple\
Search for descriptions that end with the search text| When the user may want to search for the required text at the end of words| ?| ?| Low| Moderate\
Search for words within a description in any order| When the user does not how words are ordered in the Descriptions.| ?| ?| High| Moderate\
Search for identical terms| When the user knows the exact term string that they require| ?| ?| Low| Simple\
Search for word(s) in a specific order (or a matching phrase)| When the user somewhat knows the term string that they require but not the full description| ?| ?| Medium| Moderate\
Search for Concept Identifiers| When the user wants to know the Description of the Concept that he requires| ?| ?| Low| Simple\
Search for Description Identifiers| When the user wants to knows the Concept of the Description that he requires| ?| ?| Low| Simple
