---
categories: []
layout: page
title: 'Dynamic Indexing: a Tragic Solr Story'
created: 1417819294
---
- Wayne Schneider, wschneider at hclib.org, [Hennepin County Library](//www.hclib.org)

Loading data from an ILS into Solr isn’t so hard, unless it needs to be
dynamic, fast, and hold more data than what can be found in 1.5 million
MARC records. Some additional information we’ve incorporated are from
Syndetics, ILS circulation, and OverDrive. We’ll share the nitty gritty
details and what we learned about dynamic Solr indexing, including how
to get good performance, how to deal with indexing failures, how to
schedule it all to keep the data up-to-date, and some things you can do
with that data such as popularity ratings.
