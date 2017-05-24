# case-reports

This repository contains a collection of functionsin Python 2.7 to assist with PubMed queries.

To generate a citation count distribution, use the function ```buildDistribution()``` in the file ```citation_distrib.py```.

First, define the publication set from which you wish to generate the distribution. You must specify a list of MeSH terms that are required for a publication to be included in the set. A publication need only have one of the specified MeSH terms.

Optionally, you may a specify a list of PMIDs that will be excluded from the set, as well as a range of publication dates. You may also specify whether you wish to search MeSH Terms or MeSH Major Topics.

Specify term type on line 16 and all other parameters on line 129.

The output is a map where each key is count of citations for a publication in PubMed Central (PMC), and each value is the number of publications in the queried set with that citation count. For example, the distribution

```
{'0': 23, '1': 3, '4': 2}
```

would describe a set of 29 publications, 23 of which had no citations in PMC, 3 of which had 1 publication in PMC, and 2 of which had 4 publications in PMC.

These counts represent minimum citation counts. A publication could be cited by other publications which are not tracked in PMC.
