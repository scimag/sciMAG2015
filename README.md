# sciMAG2015

### The Open data set linking Microsoft Academic Graph and sciMAGO's journal classification for bibliometrics studies.

![alt text](sciMAGviz.png "")


| Papers|Citations| Authors| Journals|Macro-areas|Sub-areas|
|:-----:|:-------:|:------:| :-----: |:---------:|:-------:|
| 35 M+ | 324 M+  |  38 M+ | 14,413  | 27        | 306     |

Papers are classified according to the journal where they have been published. 
SciMAG is built by linking the Microsoft Academic Graph and the SciMAGO Journal Classification. We classified papers into 306 distinct research topics and 27 unique knowledge areas (a coarser level of classification). The resulting data set has more than 35 million papers, cross-referencing each other more than 324 millions times.

Visit the [official Web page](https://scimag.github.io/sciMAG2015) to know more about the data set.

# Technical details

The sciMAG data set provides bibliographic information about papers published in journals in the last century (see the [official Web page](https://scimag.github.io/sciMAG2015) for further details). The data set consists of the following information. (Note that each file begins with a header, indicating the data fields)

## Main databases

### Publications

File: `paper_database_author.txt`

Format: `paperID|authorID|affiliationID`

Fields: 
	
* `paperID`: unique identifier of the paper
* `authorID`: unique identifier of the author
* `affiliationID`: unique identifier of the affiliation

Example:

	0C29797B|3E751A67|37A88C3E

File: `paper_database_journal.txt`

Format: `paperID|year|journalID`

Fields: 
	
* `paperID`: unique identifier of the paper
* `year`: publication year
* `journalID`: unique identifier of the journal

Example:

	0E05E7D1|2013|01DF587F

### Citations

File: `citation_database.txt`

Format: `fromPaperID|fromYear|fromJournalID|toPaperID|toYear|toJournalID`

Fields: 
	
* `fromPaperID`: unique identifier of the paper originating the citation
* `fromYear`: publication year of the paper originating the citation
* `fromJournalID`: venue of the paper originating the citation
* `toPaperID`: unique identifier of the paper receiving the citation
* `toYear`: publication year of the paper receiving the citation
* `toJournalID`: venue of the paper receiving the citation

Example:

	0000000D|2012|091AEFC0|034D853F|2008|06A018D9



## Metadata


### Journals

File: `journal_metadata.txt`

Format: `journalID|name|area|categ`

Fields: 
	
* `journalID`: unique identifier of the journal
* `name`: journal name
* `area`: journal knowledge area
* `categ`: journal topic category

Example:

	05B62529|Forest Policy and Economics|Agricultural and Biological Sciences$Economics, Econometrics and Finance$Environmental Science$Social Sciences|Forestry$Economics and Econometrics$Management, Monitoring, Policy and Law$Sociology and Political Science
	
Note that a single journal might be classified into one or more categories. In this case, the entries are separated by a $ char.

### Authors

File: `author_metadata.txt`

Format: `authorID|authorName`

Fields: 
	
* `authorID`: unique identifier of the paper
* `authorName`: author name

Example:

	432E2D9D|JUN ZENG

### Affiliations

File: `affiliation_metadata.txt`

Format: `affiliationID|affiliationName`

Fields: 
	
* `affiliationID`: unique identifier of the affiliation
* `affiliationName`: affiliation name

Example:

	001DD023|UNIVERSITY OF COLOMBO SCHOOL OF COMPUTING

#### Papers

File: `paper_metadata.txt`

Format: `paperID|paperTitle|year|DOI`

Fields: 
	
* `paperID`: unique identifier of the paper
* `paperTitle`: paper title
* `year`: publication year
* `DOI`: Digital Object Identifier

Example:

	0E05E7D1|THORACIC VASCULAR IMAGING: THORACIC AORTIC DISEASE AND PULMONARY EMBOLISM|2013|10.1259/IMAGING.20100064


# Copyright

The SciMAG 2015 is made available under the [Open Database License](http://opendatacommons.org/licenses/odbl/1.0/). Any rights in individual contents of the database are licensed under the [Database Contents License](http://opendatacommons.org/licenses/dbcl/1.0/). A human-readable summary of the license is available [here](http://opendatacommons.org/licenses/odbl/summary/). 

If you use the sciMAG 2015 for your research, please, cite the following papers:

	Manlio De Domenico, Elisa Omodei, Alex Arenas
	Quantifying the Diaspora of Knowledge in the Last Century.
	Applied Network Science

	Arnab Sinha, Zhihong Shen, Yang Song, Hao Ma, Darrin Eide, Bo-June (Paul) Hsu, and Kuansan Wang. 2015.
	An Overview of Microsoft Academic Service (MAS) and Applications.
	In Proceedings of the 24th International Conference on World Wide Web (WWW ’15 Companion).
	ACM, New York, NY, USA, 243-246. DOI=10.1145/2740908.2742839

# Support or Contact

Having trouble with SciMAG? Send an email to [Manlio De Domenico](mailto:manlio.dedomenico@urv.cat)

