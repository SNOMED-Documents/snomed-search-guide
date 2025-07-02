# Order Search Results Rationally

This section concerns the rational ordering of search results. When developing browsers and search embedded functionality within clinical applications, careful consideration must be taken in specifying the prioritization of search results, as adopting many of the recommended techniques below may compromise the speed of search.

## Order Shortest Matching Terms First

Ordering the shortest matching term first is a common display requirement for search browsers and search functionalities in clinical applications. This applies text search techniques previously in the Guide (e.g. searching for descriptions that contain the search text). \[see 4.1.1 Search by text] Many users can expect this technique to exist in all use cases concerning searches that return large result sets. It is intuitive to display the shortest term that is also the closest lexical match first. If the shortest matching term is not in the first set of visible matches, a user is likely to assume that there are no relevant candidate matches or use the wrong concept or description.

<figure><img src="../../images/52170502.png" alt=""><figcaption><p>Figure 5.1.1-1: Ordering shortest matching terms first</p></figcaption></figure>

A common mistake is to implement a search functionality that is configured to sort search results alphabetically in a clinical setting. The result list, when Concepts like hernia is searched, starts as shown below and the term "hernia" itself would be more than 130 items down a list of over 700 matches.

Table 5.1.1-1: Position of term 'hernia' in an alphabetic and shortest terms ordered search 'hernia'

**Position**| **Alphabetic order of results**| \*\*Shortest match first\
\*\*\
\---|---|---\
1| abdominal hernia| **hernia**\
2| abdominal wall hernia procedure| hernia sac\
3| airway device cuff herniation| hernia belt\
4| anesthesia for hernia repair in lower abdomen| O/E - hernia\
...| anesthesia for hernia repair in upper abdomen| cecal hernia\
6| anesthesia for lumbar or ventral incisional hernia of upper abdomen| labial hernia\
7| anesthesia for transabdominal repair of diaphragmatic hernia| hernia repair\
8| anesthesia for ventral or incisional hernia repair, lower abdomen| littré hernia\
9| anterior perineal hernia| Cooper hernia\
....|\
|

**131**| **hernia**|

{% hint style="danger" %}
**Caution**

Alphabetic searches can compromise patient safety as the best matching term is not easily found. However, even searches for the shortest term need to be constrained to concept types relevant to the clinical setting to ensure only relevant matches are shown.
{% endhint %}

## Order Preferred Term Matches Before Synonyms

It is recommended to order preferred term matches before synonyms, particularly in clinical settings, as the _Preferred Term_ is a common word or phrase used by clinicians to name that _Concept_. This technique will enhance usability and significantly increase the speed of data entry. It may be helpful to the user whether the candidate match is a Preferred Term or synonym.

<figure><img src="../../images/52170504.png" alt=""><figcaption><p>Figure 5.1.2-1: Ordering preferred term matches before synonyms</p></figcaption></figure>

## Order User Preferred Term Language Matches First in Multilingual Environments

For a country or region that has more than one official language (e.g. Belgium), it would be useful to have a user configurable option that enables results to display matches in a preferred language first in applications that support more than one language. This can be done using combinations of Language Reference Sets.

## Order According to Priority in Any Active Reference Sets

Search results may need to be configured in a specified order using one or more active Ordered Reference Sets. The way in which access to search results is prioritized depends on the nature of the application and its operating environment. Examples of prioritization include:

* Showing Descriptions associated with high priority Concepts before those with lower priority.
* Showing Concepts with high priority before their less highly prioritized siblings in hierarchical display results. \[see 5.5.3 Using the navigation hierarchy]
* Initially listing Concepts and associated Descriptions with priority above a specified threshold and requiring additional step to access those assigned lower priority.

<figure><img src="../../images/52170507.png" alt=""><figcaption><p>Figure 5.1.4-1: Unordered search results for cranial nerve</p></figcaption></figure>

<figure><img src="../../images/52170506.png" alt=""><figcaption><p>Figure 5.1.4-2: Ordering search results for cranial nerve using and ordered component reference set</p></figcaption></figure>

## Display the Most Frequently Used Descriptions Listed First

This option will require the application to track the frequency of term selection so that search results can show the most frequently selected terms near the top of the results or displayed separately in the results. If this technique is chosen, user guidance may be necessary to minimize the risk of overusing the frequently used Descriptions as they would be easier to find. An alternative way of browsing through frequently used terms is to give the user the option to store the frequently selected terms as personal favorites and recall with user-defined abbreviated access term following a search. \[see Use Mnemonics and personal favorites for data entry]

<figure><img src="../../images/52170509.png" alt=""><figcaption><p>Figure 5.1.5-1: Displaying most frequently used Description after this Description was entered in previous search</p></figcaption></figure>

## Alphabetical Ordering

As noted in the [Order Shortest Matching Terms First ](./#order-shortest-matching-terms-first)section, alphabetical ordering of search results should **NOT** be used for general purpose searches of SNOMED CT. Instead the shortest matches, best matches or most commonly used matches should be shown first. However, there may be some specific situations in which it may be useful to alphabetically order a short list of matches. For example short pick-lists may be alphabetically ordered in a data entry form. \[see [Examples of applied mechanisms of structured data entry](<../../6 data-entry/6.2 structured-data-entry/6.2.5-examples-of-applied-mechanisms-of-structured-data-entry.md>)]
