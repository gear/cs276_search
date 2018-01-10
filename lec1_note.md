## Lecture 1: Boolean Retrieval

**Boolean Retrieval model** is being able to as k a query that is a Boolean
expression (AND, OR, NOT). WestLaw is an example of professional Boolean 
search system. Example search query: `LIMIT! /3 STATUE ACTION /S FEDERAL /2 
TORT /3 CLAIM`. This search query contains proximity search (within 2 or 3
words). 

**The classic search model** (page 6, lec1 slide). Translating from user task
to info need is prone to misconception. Precision is the fraction of retrieved
docs that are relevant to the user's information need. Recall is the fraction
of relevant docs in collection that are retrieved.

**Merge** operation is a standard in search query. The time complexity for a
AND operation is typically O(x+y), where x and y are the lengths of documents
listing of the two terms.

**Postional index** is now standardly used because of the power and usefulness of 
the phrase and proximity queries. Positional index, in a nutshell, is to store 
a dictionary of terms pointing to document ids. Each document ids then points 
to a list of the position of that term in the document. Such representation 
allows proximity queries.

- Positional index is 2-4 times as large as non-positional index.
- Positional index size is 35-50% of original text volume.
- Combination schemes can speed up querying time by 4 (Williams et al., 2004).
It requires 26% more space than having a positional index alone. E.g. Phrases
like "Michael Scott" or "Albert Einstein" should be stored in biword index
since it is inefficient to keep on merging positional posting list. 

## Reading IIR 1

**Information retrieval systems** can be distinguished by the scale at
which they operate:
1. Web search: Contains billions of documents, stored on millions of computers.
Issues: Crawling for indexing, efficiency at large scale, handling hypertext,
handling SEO.
2. Personal information retrieval: Personal files or emails, stored on a 
single computer. Issues: Heterogeneous nature of multimedia files, 
efficiency at limited processing power.
3. Enterprise: Specialized information, stored on a number of dedicated 
machines.
