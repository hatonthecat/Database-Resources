
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

This local host is with just SQLite installed, but other dBs like PostgreSQL and MySQL can be installed (based on the type of DB). The above one, HDC, uses MySQL.

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

--------
3/20/23
--------
Just learned strikethrough is an option on Github. ~~This is a test~~. If Strikethrough appears, additional edits are not required. Strikethrough has many benefits, as 
it doesn't require the average read to look into the history to see changes and corrections made. Also, this is a rule in science notebooks, which helps understand what happened in an experiment:

"https://openwetware.org/wiki/BISC110/F13:Guidelines_for_maintaining_your_lab_notebook
"• If you make mistakes, do NOT obliterate the error; instead, strike-through once. Never erase, use "white-out," or tear out pages. It is fine to strike-through or X-out (once!) whole pages if it is necessary to start over. You must use an indelible pen to write in your lab notebook. It would not be of much use as a legal document if it were written in pencil.""

In the digital age, some of these practices can't always be practiced, but as a general rule, it helps with science having an open methods. Secondly, certain databases that I have great interest in do not all have record keeping for every query in a write-through, such as a lmdb: http://www.lmdb.tech/doc/

I am interested in several DBS, like leveldb: https://github.com/google/leveldb

I haven't actually found the exact type of DB, but there are things I like about several of them, such as Apache Kafka:
https://en.wikipedia.org/wiki/Apache_Kafka

"Kafka uses a binary TCP-based protocol that is optimized for efficiency and relies on a "message set" abstraction that naturally groups messages together to reduce the overhead of the network roundtrip. This "leads to larger network packets, larger sequential disk operations, contiguous memory blocks [...] which allows Kafka to turn a bursty stream of random message writes into linear writes."[3]"

Also on my check-out list (not check out cart, but "check out"):

Length-prefixed JSON 

missive Fast, lightweight library for encoding and decoding length-prefixed JSON messages over streams"
https://en.wikipedia.org/wiki/JSON_streaming#Introduction

https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/Native_messaging

MQTT and SQLite: 
http://www.steves-internet-guide.com/logging-mqtt-sensor-data-to-sql-database-with-python/

M2M MQTT Broker: https://www.hivemq.com/blog/mqtt-sql-database/
http://www.steves-internet-guide.com/mqtt-sn/
https://www.eclipse.org/paho/

And some Java based frameworks:

https://github.com/quarkusio/quarkus


