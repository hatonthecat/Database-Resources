
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
it doesn't require the average reader to look into the history to see changes and corrections made. Also, this is a rule in science notebooks, which helps understand what happened in an experiment:

"https://openwetware.org/wiki/BISC110/F13:Guidelines_for_maintaining_your_lab_notebook
"• If you make mistakes, do NOT obliterate the error; instead, strike-through once. Never erase, use "white-out," or tear out pages. It is fine to strike-through or X-out (once!) whole pages if it is necessary to start over. You must use an indelible pen to write in your lab notebook. It would not be of much use as a legal document if it were written in pencil.""

In the digital age, some of these practices can't always be ~~practiced~~ realized, but as a general rule, it helps with science having an open methods. Secondly, certain databases that I have great interest in do not all have record keeping for every query in a write-through, ~~such as lmdb~~

case in point: ![image](https://user-images.githubusercontent.com/76194453/226452110-06a65923-c9ee-46d0-8ef4-dd41adf93ce9.png)
 
So i have added more strike through characters, according to the original instuctions, which say to use ~ before and after each word, 2 flanking each side.

(I swear the strike through appeared to be working in the editor but I created a new line and changed it since striking through each word was confusing and not quite working) :http://www.lmdb.tech/doc/

"The entire database is exposed in a memory map, and all data fetches return data directly from the mapped memory, so no malloc's or memcpy's occur during data fetches. As such, the library is extremely simple because it requires no page caching layer of its own, and it is extremely high performance and memory-efficient. It is also fully transactional with full ACID semantics, and when the memory map is read-only, the database integrity cannot be corrupted by stray pointer writes from application code."

From a purely experimental perspective, I believe performance can be explored first, then recording abilities second. Recording is certainly useful although it doesn't appear necessary unless it is the only way to prove that the information retrieval is accurate and not prone to data-copy/read/write/ error.


I am more interested in combining all layers and aspects of non-essential, non-ACID compliant DBs in a UDP manner using RESTful async- with Ajax https://en.wikipedia.org/wiki/Ajax_(programming) that is, a DB requiring as little sync as possible to complete a query. Part of the puzzle is finding the simplest protocol in each layer.

A hypothetical DB returning just a single key value after querying a different key would represent the simplest transactional DB. Client-side translation services (an index, a legend, a key) would be able to provided additional bandwidth savings for minimizing/eliminating redundant query data.

For example, a daily horoscope website:

I wanted to make a super simple database where people could get their horoscope, there would only be 12 (assuming the standard type). But let's say, a fortune teller writes 365x12 horoscopes and publishes them Dec 31st of each year. Users could download the entire anthology, but for symbolic purposes, they'd need to query locally or the server a single key to search their horoscope for the day. This stories change daily, but all users would have to type in is a letter, all for the first through last astrological sign of the year. The front end would have additional browser conversion tools so it would convert the string into a letter, if they prefer to type in the word (like Taurus), (but search suggestion, a list to click on, or a drop down menu could be used as well). Plus the site wouldn't fetch other website data from the same db, only the query.

This could use a simpler text format than unicode, to save on binary data. So perhaps ascii https://en.wikipedia.org/wiki/ASCII#Bit_width
Ita2, though the DB software itself may be using Unicode so that may not be possible.

Anyways, leveldb, can handle 200k,-400k writes per second, so I am curious if I could host a web server where queries from unique up addresses are a alotted one search per minute (to limit traffic) so that it could gather up the queries in a batch in approximately 20-30 seconds, then return the results while locking the DB for writing.

This could be useful in cases where sending the entire horoscope for all 12 possibilities are bandwidth and memory intensive, and for that, I'd have a separate key, client side (on the website). The key value db would return a unique result for that day (determined only a day or two on advance, a-l)

[https://github.com/google/leveldb](https://github.com/google/leveldb#write-performance)



I haven't actually found the exact type of DB, but there are things I like about several of them, such as Apache Kafka:
https://en.wikipedia.org/wiki/Apache_Kafka (this perhaps could improve the write speed of queries- by completing them in batches- waiting enough time for queries to populate, although this would ~~not~~ necessarily be faster for the user, although it might reduce the wear on the drive).

NVMe failure rates (4 year data from Backblaze): https://arstechnica.com/gadgets/2023/03/new-data-tracks-failure-rates-of-13-ssd-models-going-back-up-to-4-years/

Amazon's Nitro offloads some of the compute to PCI-e cards, which is also interesting since it wouldn't have as much of a CPU bottleneck:
https://www.semianalysis.com/p/amazons-cloud-crisis-how-aws-will

It'd be interesting to see an LMDB running on a Raspberry Pi or similar SoC in RAM that achieves a record number of OPs or writes/second, provided the nand flash/microsd isn't required for the DB to access during the main DB function. 

"Kafka uses a binary TCP-based protocol that is optimized for efficiency and relies on a "message set" abstraction that naturally groups messages together to reduce the overhead of the network roundtrip. This "leads to larger network packets, larger sequential disk operations, contiguous memory blocks [...] which allows Kafka to turn a bursty stream of random message writes into linear writes."[3]"

Also on my check-out list (not check out cart, but "check out"):

Length-prefixed JSON 

"missive - Fast, lightweight library for encoding and decoding length-prefixed JSON messages over streams"
https://en.wikipedia.org/wiki/JSON_streaming#Introduction

https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/Native_messaging

MQTT and SQLite: 
http://www.steves-internet-guide.com/logging-mqtt-sensor-data-to-sql-database-with-python/

M2M MQTT Broker: https://www.hivemq.com/blog/mqtt-sql-database/
http://www.steves-internet-guide.com/mqtt-sn/
https://www.eclipse.org/paho/

And some Java based frameworks:

https://github.com/quarkusio/quarkus

---
3:29PM
---

"Production? Where we're going, we won't need Production" -Not Back to the Future

"The purpose of borderline useful is ability to know what's borderline." -Nobody

--
3:49 PM
--

I have an interest in DBs, but I have no specific bias of what to develop, since I have no prior knowledge of how they work. In an abstract sense, databases can be designed to meet a one-size fits many, or a very specific application. I think it is more interesting to develop a DB for a very specific use-case. However, even finding a specific use can be difficult. Instead of spending all my time looking for specific use cases, I can hypothesize more abstract databases, and try to hybridize concepts (regardless of new or old) that have not been hybridized before. Classsic Mendelian genetics.

Mendelian DBs. I should say. But the other concept above is more like Occam's Razor. so it could be called Occam's DB, or MendelDB, or MendelOcs (like Dev Ops but Dev Ocs)
