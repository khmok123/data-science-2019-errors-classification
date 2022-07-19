# Bug classification

This repository contains the source code of the group project for the course *Data Science and Big Data Analytics* held in Georg-August-Universität Göttingen in winter semester 2019. 

## Project description
For the project, we were given access to a database that was actively used for the research on open source software development. The database contains information collected from the version control system, the issue tracker, and the mailing lists of the projects. (documentation of the available data online: https://smartshark2.informatik.uni-goettingen.de/documentation/)

The database contains data for many Apache Projects. For this group project, only the following 39 projects are relevant:
- ant-ivy, archiva, calcite, cayenne, commons-bcel, commons-beanutils, commons-codec, commons-collections, commons-compress, commons-configuration, commons-dbcp, commons-digester, commons-io, commons-jcs, commons-jexl, commons-lang, commons-math, commons-net, commons-rdf, commons-scxml, commons-validator, commons-vfs, deltaspike, eagle, giraph, gora, jspwiki, kylin, lens, mahout, manifoldcf, nutch, opennlp, parquet-mr, santuario-java, systemml, tika, wss4j

Our task is to develop an automated model for the classification of issues as bugs. The model should be designed in such a way that it could be applied upon creation of an issue, i.e., as a recommendation system for users of the issue tracking system. 

## Implementation
The text mining procedures were performed on the bug messages (removing punctuations, cases and stop words, stemming and lemmatization) and the bag-of-words models were used to transform the corpuses to arrays. After trials using different machine learning models, the multinomial naive Beyes model gives the best result with an accuracy of 60% (nearly 80% for binary data). 
