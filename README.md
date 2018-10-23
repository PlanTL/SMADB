# SmaDB: Spanish Medical Abbreviation DataBase

## Introduction

This repository contains the Spanish Medical Abbreviation DataBase. 
This database is created automatically by detecting abbreviations and their potential definitions explicitly mentioned in the same sentence. These abbreviations are extracted from the metadata of different biomedical publications written in Spanish, which contain the titles and abstracts. 
The sources of these publications are SciELO[1], IBECS[2] and Pubmed[3]. 
The chosen schema is Dublin Core (http://dublincore.org/). We use the official ones from SciELO, and customized adaptations of the XML files to Dublin Core from IBECS and Pubmed metadata. 
The source code used to generate this resources is available here https//github.com/PlanTL/SMADDB-generator.

## Directory structure

<pre>
abbreviations.tsv
This file gathers all abbreviations in the database and displays information about them. Each column is 
structured the following way:
  - Abbreviation ID.
  - Frequency: the number of times the abbreviation has been detected in the corpora, together with 
  the definition in the same sentence.
  - Abbreviation: the abbreviation in string format.
  - Definitions: definition IDs where the abbreviation has been associated to.
  - Appears on: publication IDs where the abbreviation has been mentioned.

definitions.tsv
This file gathers all definitions in the database and displays information about them. Each column is 
structured in the following way:
  - Definition ID.
  - Frequency: the number of times the definition has been detected in the corpora, together with 
  the abbreviation in the same sentence.
  - Definition: the definition in string format.
  - Abbreviations: abbreviation IDs where the definition has been associated to.
  - Appears on: publication IDs where the definition has been mentioned.

pairs.tsv
This file gathers all abbreviation-definition pairs found in the corpora and displays information 
about them. Each column is structured in the following way:
  - Pair ID.
  - Abbreviation ID.
  - Definition ID.
  - Frequency: the number of times this abbreviation-definition pair has been detected in the corpora.
  - Abbreviation: abbreviation in string format.
  - Definition: definition in string format.
  - Appears on: publication IDs where we the pair is mentioned.

</pre>

## Contact

Ander Intxaurrondo (ander.intxaurrondo@bsc.es)


## License

(This is so-called MIT/X License)

Copyright (c) 2017-2018 Secretaría de Estado para el Avance Digital (SEAD)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## References

[1] Y. Yamamoto, A. Yamaguchi, H. Bono and T. Takagi, "Allie: a database and a search service of abbreviations and long forms.", http://allie.dbcls.jp/

[2] Scientific Electronic Library Online (SciELO Spain) is an electronic virtual library covering a collection of Spanish health scientific journals selected following preestablished quality criteria. Developed and maintained by the Spanish National Library of Health Sciences.  http://scielo.isciii.es

[3] Bibliographical database for health articles, contains abstracts and references of different articles written in Spanish. Developed and maintained by the Carlos III Health Institute in Madrid, Spain. http://ibecs.isciii.es

[4] PubMed is a free search engine accessing primarily the MEDLINE database of references and abstracts on life sciences and biomedical topics. The United States National Library of Medicine (NLM) at the National Institutes of Health maintains the database as part of the Entrez system of information retrieval. https://www.ncbi.nlm.nih.gov/pubmed/

[5] A.S. Schwartz, M.A. Hearst, "A Simple Algorithm for Identifying Abbreviation Definitions in Biomedical Text"
