---
excerpt: "<strong>How to Implement A Virtual Bookshelf With Solr</strong>\r\n\r\n<ul>\r\n<li>Naomi
  Dushay, Stanford University, ndushay@stanford.edu</li>\r\n<li>Jessie Keck, Stanford
  University, jkeck@stanford.edu </li>\r\n</ul>\r\n\r\n<a href=\"/conference/2010/schedule\">Code4Lib
  2010</a> - Wednesday, February 24 - 14:00-14:20\r\n\r"
categories:
- conferences
- code4lib 2010
layout: page
title: How to Implement A Virtual Bookshelf With Solr - Naomi Dushay and Jessie Keck
  - Code4Lib 2010
created: 1267076411
---
<strong>How to Implement A Virtual Bookshelf With Solr</strong>

<ul>
<li>Naomi Dushay, Stanford University, ndushay@stanford.edu</li>
<li>Jessie Keck, Stanford University, jkeck@stanford.edu </li>
</ul>

<a href="/conference/2010/schedule">Code4Lib 2010</a> - Wednesday, February 24 - 14:00-14:20

Browsing bookshelves has long been a useful research technique as well as an activity many users enjoy. As larger and larger portions of our physical library materials migrate to offsite storage, having a browse-able virtual shelf organized by call number is a much-desired feature. I will talk about how we implemented nearby-on-shelf in Blacklight at Stanford, using Solr and SolrMarc:

<ol>
<li>the code to get shelfkeys out of call numbers</li>
<li>the code to lop volume data off the end of call numbers to avoid clutter in the browse</li>
<li>what I indexed in Solr given we have</li>
<ol>
<li>multiple call numbers for a single bib record</li>
<li>multiple bib records for a single call number </li>
</ol>
<li>Solr configuration, requests and responses to get call numbers before and after a given starting point as well as the desired information for display.</li>
<li>Other code needed to implement this feature in Blacklight (concepts easily ported to other UIs).</li>
</ol>

This virtual shelf is not only browsable across locations, but includes any item with a call number in our collection (digital or physical materials). 


Naomi says:  "Some of this code is available in SolrMarc trunk as of 2010-02-28, but with the upgrade to SolrMarc version 2.1, the stanfordBlacklight example will probably not be up to date for a few weeks.  The Blacklight part of the code will also be forthcoming."

(Presentation)
<a href="http://www.stanford.edu/people/~ndushay/code4lib2010/stanford_virtual_shelf.pdf">http://www.stanford.edu/people/~ndushay/code4lib2010/stanford_virtual_shelf.pdf</a>

Stanford's <a href="searchworks.stanford.edu">SearchWorks</a> Solr configuration files:
<ul>
 <li>conf/schema.xml <a href="http://www.stanford.edu/people/~ndushay/code4lib2010/stanford/schema.xml">http://www.stanford.edu/people/~ndushay/code4lib2010/stanford/schema.xml</a></li>
 <li>conf/solrconfig.xml <a href="http://www.stanford.edu/people/~ndushay/code4lib2010/stanford/solrconfig.xml">http://www.stanford.edu/people/~ndushay/code4lib2010/stanford/solrconfig.xml</a></li>
 <li>solrmarc sw_index.properties (note there is custom code used not yet checked into StanfordBlacklight example in SolrMarc project) <a href="http://www.stanford.edu/people/~ndushay/code4lib2010/stanford/sw_index.properties">http://www.stanford.edu/people/~ndushay/code4lib2010/stanford/sw_index.properties</a></li>
  <li>if you want more information about our Solr index or our Marc -> Solr code, please send me an email.</li>
</ul>
