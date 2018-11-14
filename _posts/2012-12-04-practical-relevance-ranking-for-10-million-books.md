---
excerpt: "<strong>Practical Relevance Ranking for 10 million books</strong>\r\n\r\n<ul>\r\n<li>Tom
  Burton-West, University of Michigan Library, tburtonw@umich.edu</li>\r\n</ul>\r\n\r\n<a
  href=\"http://www.hathitrust.org/\">HathiTrust Full-text search</a> indexes the
  full-text and metadata for over 10 million books. There are many challenges in tuning
  relevance ranking for a collection of this size. This talk will discuss some of
  the underlying issues, some of our experiments to improve relevance ranking, and
  our ongoing efforts to develop a principled framework for testing changes to relevance
  ranking.\r\n\r\nSome of the topics covered will include:\r\n<ul>\r\n<li>Length normalization
  for indexing the full-text of book-length documents</li>\r\n<li>Indexing granularity
  for books</li>\r\n<li>Testing new features in Solr 4.0: \r\n    <ul>\r\n      <li>New
  ranking formulas that should work better with book-length documents: BM25 and DFR.</li>
  \r\n      <li>Grouping/Field Collapsing. Can we index 3 billion pages and then use
  Solr's field collapsing feature to rank books according to the most relevant page(s)?
  </li>\r\n      <li>Finite State Automota/Block Trees for storing the in-memory index
  to the index. Will this allow us to allow wildcards/truncation despite over 2 billion
  unique terms per index?</li>\r\n    </ul>\r"
categories:
- conferences
- code4lib 2013
layout: post
title: Practical Relevance Ranking for 10 million books.
created: 1354662285
---
<strong>Practical Relevance Ranking for 10 million books</strong>

<ul>
<li>Tom Burton-West, University of Michigan Library, tburtonw@umich.edu</li>
</ul>

<a href="http://www.hathitrust.org/">HathiTrust Full-text search</a> indexes the full-text and metadata for over 10 million books. There are many challenges in tuning relevance ranking for a collection of this size. This talk will discuss some of the underlying issues, some of our experiments to improve relevance ranking, and our ongoing efforts to develop a principled framework for testing changes to relevance ranking.

Some of the topics covered will include:
<ul>
<li>Length normalization for indexing the full-text of book-length documents</li>
<li>Indexing granularity for books</li>
<li>Testing new features in Solr 4.0: 
    <ul>
      <li>New ranking formulas that should work better with book-length documents: BM25 and DFR.</li> 
      <li>Grouping/Field Collapsing. Can we index 3 billion pages and then use Solr's field collapsing feature to rank books according to the most relevant page(s)? </li>
      <li>Finite State Automota/Block Trees for storing the in-memory index to the index. Will this allow us to allow wildcards/truncation despite over 2 billion unique terms per index?</li>
    </ul>
<li>Relevance testing methodologies:Query log analysis, Click models, Interleaving, A/B testing, and Test collection based evaluation.</li>
<li>Testing of a new high-performance storage system to be installed in early 2013. We will report on any tests we are able to run prior to conference time.</li>
</ul>

Download slides: <a href="http://www.hathitrust.org/documents/HathiTrust-Code4LIB-201302.pptx">http://www.hathitrust.org/documents/HathiTrust-Code4LIB-201302.pptx</a>
<br></br>

<video controls="" poster="https://ia801600.us.archive.org/33/items/Day2TomBurtonWest/Day2-Tom%20Burton-West.gif"><source src="https://ia801600.us.archive.org/33/items/Day2TomBurtonWest/Day2-Tom%20Burton-West.mp4" type="video/mp4"><source src="https://ia801600.us.archive.org/33/items/Day2TomBurtonWest/Day2-Tom%20Burton-West.ogv" type="video/ogg"></video><p><a href="https://ia801600.us.archive.org/33/items/Day2TomBurtonWest/Day2-Tom%20Burton-West.mp4">Download the video</a></p>
