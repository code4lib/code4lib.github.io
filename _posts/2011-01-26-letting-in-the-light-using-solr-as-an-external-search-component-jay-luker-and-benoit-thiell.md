---
excerpt: "<strong>Letting In the Light: Using Solr as an External Search Component
  </strong>\r\n\r\n<ul>\r\n<li><a href=\"http://www.slideshare.net/lbjay/letting-in-the-light-using-solr-as-an-external-search-component\">Slides</a></li>\r\n<li><a
  href=\"http://www.indiana.edu/~video/stream/launchflash.html?format=MP4&folder=vic&filename=C4L2011_session_2_20110208.mp4\">Archived
  Video</a> [time: 241:45]</li>\r\n</ul>\r\n\r\n<ul>\r\n<li> Jay Luker, IT Specialist,
  ADS, jluker@cfa.harvard.edu</li>\r\n<li> Benoit Thiell, software developer, ADS,
  bthiell@cfa.harvard.edu</li>\r\n</ul>\r\n\r"
categories:
- code4lib 2011
layout: page
title: 'Letting In the Light: Using Solr as an External Search Component - Jay Luker
  and Benoit Thiell'
created: 1296086640
---
<strong>Letting In the Light: Using Solr as an External Search Component </strong>

<ul>
<li><a href="http://www.slideshare.net/lbjay/letting-in-the-light-using-solr-as-an-external-search-component">Slides</a></li>
<li><a href="http://www.indiana.edu/~video/stream/launchflash.html?format=MP4&folder=vic&filename=C4L2011_session_2_20110208.mp4">Archived Video</a> [time: 241:45]</li>
</ul>

<ul>
<li> Jay Luker, IT Specialist, ADS, jluker@cfa.harvard.edu</li>
<li> Benoit Thiell, software developer, ADS, bthiell@cfa.harvard.edu</li>
</ul>

<a href="/conference/2011/schedule">Code4Lib 2011</a>, Tuesday 8 February, 14:30 - 14:50

It’s well-established that <a href="http://lucene.apache.org/solr/" title="http://lucene.apache.org/solr/" rel="nofollow">Solr</a> provides an excellent foundation for building a faceted search engine. But what if your application’s foundation has already been constructed? How do you add Solr as a federated, fulltext search component to an existing system that already provides a full set of well-crafted scoring and ranking mechanisms?

This talk will describe a work-in-progress project at the <a href="http://adswww.harvard.edu/" title="http://adswww.harvard.edu/" rel="nofollow">Smithsonian/NASA Astrophysics Data System</a> to migrate its aging search platform to <a href="http://invenio-software.org/" title="http://invenio-software.org/" rel="nofollow">Invenio</a>, an open-source institutional repository and digital library system originally developed at CERN, while at the same time incorporating Solr as an external component for both faceting and fulltext search.

In this presentation we'll start with a short introduction of Invenio and then move on to the good stuff: an in-depth exploration of our use of Solr. We'll explain the challenges that we faced, what we learned about some particular Solr internals, interesting paths we chose not to follow, and the solutions we finally developed, including the creation of custom Solr request handlers and query parser classes.

This presentation will be quite technical and will show a measure of horrible Java code. Benoit will probably run away during that part.

