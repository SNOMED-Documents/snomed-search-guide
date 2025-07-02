# 4. Optimizing Searches

Today, a variety of general purpose text search tools and software libraries are in everyday use. Many of these general techniques can be applied to SNOMED CT though this does not automatically mean that they should be or that they are sufficient. Optimal indexing of SNOMED CT Descriptions may require a customized indexing solution. There are several widely available SNOMED CT browsers and related search tools, some of which use general purpose search techniques, and others which use some of the specific features discussed in this section. However, SNOMED CT searches often result in a very long list of terms, complete with additional information which must be assessed to fully understand the difference between terms in the search results. For example, searching for "diabetes" in most browsers returns a long list of lexical matches from multiple sub-type hierarchies. Choosing the appropriate term from this list can be a challenge if the terminological context is not apparent from the list.

Effective implementation of SNOMED CT depends on the speed and simplicity with which users can locate the terms and Concepts that they wish to use. A busy clinical user may become frustrated if the content they need cannot be quickly located when they search using familiar words or phrases. For this reason an efficient search strategy should address the many of the following key issues:

* Search should not be too sensitive to word order or exact phrasing:
  * Search should be insensitive to word - order variants:
    * For example, "head pain" for | pain in head |
  * Allow use of acronyms or abbreviations for frequently used terms:
    * For example, "MI" for "myocardial infarction" or "mitral incompetence".
* Excessive search results should not hinder selection of the required Concept:
  * When several synonyms of the same Concept match the search key, only one may need to be displayed.
* Speed result ordering
* Speed of search:
  * Search speed should be optimized
    * For example, use appropriate indexes (e.g. single key index).

The purpose of this section is to describe various strategies that might be used to implement the search requirements outlined above. A balance must be kept between the completeness and specificity of searches. Therefore, the next sections consider techniques that extend searches to improve completeness and techniques that constrain searches to improve specificity.
