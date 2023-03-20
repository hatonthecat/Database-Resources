
https://cosmograph.app/

https://en.wikipedia.org/wiki/Graph_database#List_of_graph_databases

https://neo4j.com/docs/getting-started/current/get-started-with-neo4j/graph-database/

https://memgraph.com/

https://www.tigergraph.com/

3/19/2023: 
Was interested in seeing how discovery interfaces work with DB (e.g. library search front-ends) like https://github.com/harvard-lts/HarvardDigitalCollections

The software is called Blacklight: https://github.com/projectblacklight/blacklight 
so I set up Ruby on Rails on Ubuntu 22.04 in WSL (now available in the Windows Store): https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-11-with-gui-support#1-overview
using this guide: 
https://gorails.com/setup/ubuntu/22.04#ruby (Great, simple tutorial)
![image](https://user-images.githubusercontent.com/76194453/226226211-c2670572-f576-4772-86ab-0c45c3e4f147.png)

This local host is with just SQLite installed, but other dBs like PostgreSQL and MySQL can be installed (based on the type of DB). The above one HDC, uses MySQL.

Next step would be to install Apache Solr, which is based on Apache Lucene: https://github.com/apache/solr  

Another useful package is Bundler, although this appears to be optional: https://bundler.io/ 

https://github.com/projectblacklight/blacklight/wiki/Quickstart  

Next step is to install Java $ https://github.com/projectblacklight/blacklight/wiki/Quickstart#got-java 

and then SolrMARC, https://github.com/solrmarc/solrmarc https://github.com/marc4j/marc4j 

then the data itself: https://en.wikipedia.org/wiki/MARC_standards
https://www.oclc.org/bibformats/en/introduction.html

It would be interesting to see what DBs could work well with nano-publications once I get this all up and running:
https://www.w3.org/wiki/images/c/c0/HCLSIG$$SWANSIOC$$Actions$$RhetoricalStructure$$meetings$$20100215$cwa-anatomy-nanopub-v3.pdf

https://www.w3.org/wiki/images/4/4a/HCLS$$ISWC2009$$Workshop$Mons.pdf

https://peerj.com/articles/cs-78/ 

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4786890/

https://www.consultmu.co.uk/single-figure-publications-and-nano-publications/

https://f1000research.com/

Some formats for nano-pub are RDF, which can be converted into CSV: https://github.com/linkedpipes/etl which can be converted into SQLite:

https://www.sqlitetutorial.net/sqlite-import-csv/ using SQLStudio: https://sqlitestudio.pl/



