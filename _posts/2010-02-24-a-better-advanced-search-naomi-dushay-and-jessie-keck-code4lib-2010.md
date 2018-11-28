---
excerpt: "<strong>A Better Advanced Search</strong>\r\n\r\n<ul>\r\n<li>Naomi Dushay,
  Stanford University, ndushay@stanford.edu</li>\r\n<li>Jessie Keck, Stanford University,
  jkeck@stanford.edu </li>\r\n</ul>\r\n\r\n<a href=\"/conference/2010/schedule\">Code4Lib
  2010</a> - Wednesday, February 24 - 13:00-13:20\r\n\r"
categories:
- conferences
- code4lib 2010
layout: post
title: A Better Advanced Search - Naomi Dushay and Jessie Keck - Code4Lib 2010
created: 1267075737
permalink: /conference/2010/dushay_keck/
---
<strong>A Better Advanced Search</strong>

<ul>
<li>Naomi Dushay, Stanford University, ndushay@stanford.edu</li>
<li>Jessie Keck, Stanford University, jkeck@stanford.edu </li>
</ul>

<a href="/conference/2010/schedule">Code4Lib 2010</a> - Wednesday, February 24 - 13:00-13:20

Even though we'd love to get basic searches working so well that advanced search wouldn't be necessary, there will always be a small set of users that want it, and there will always be some library searching needs that basic searching can't serve. Our user interface designer was dissatisfied with many aspects of advanced search as currently available in most library discovery software; the form she designed was excellent but challenging to implement. See http://searchworks.stanford.edu/advanced We'll share details of how we implemented Advanced Search in Blacklight:

<ol>
<li>non-techie designed html form for the user</li>
<li>boolean syntax while using Solr dismax magic (dismax does not speak Boolean)</li>
<li>checkbox facets (multiple facet value selection)</li>
<li>fielded searching while using Solr dismax magic (dismax allows complex weighting formulae across multiple author/title/subject/... fields, but does not allow "fielded" searching in the way lucene does) - easily configured in solrconfig.xml </li>
<li>manipulating user entered queries before sending them to Solr</li>
<li>making advanced search results look like other search results: breadcrumbs, selectable facets, and other fun.</li>
</ol>

(Presentation)
I'm sure slides will be made available on the code4lib site, but in the meantime, you can see them at <a href="http://www.stanford.edu/people/~ndushay/code4lib2010/advanced_search.pdf">http://www.stanford.edu/people/~ndushay/code4lib2010/advanced_search.pdf</a>

The document explaining the specifics of the Solr queries is <a href="http://www.stanford.edu/people/~ndushay/code4lib2010/advSearchSolrQueries.pdf">http://www.stanford.edu/people/~ndushay/code4lib2010/advSearchSolrQueries.pdf</a>

Stanford's <a href="searchworks.stanford.edu">SearchWorks</a> Solr configuration files:
<ul>
 <li>conf/schema.xml <a href="http://www.stanford.edu/people/~ndushay/code4lib2010/stanford/schema.xml">http://www.stanford.edu/people/~ndushay/code4lib2010/stanford/schema.xml</a></li>
 <li>conf/solrconfig.xml <a href="http://www.stanford.edu/people/~ndushay/code4lib2010/stanford/solrconfig.xml">http://www.stanford.edu/people/~ndushay/code4lib2010/stanford/solrconfig.xml</a></li>
 <li>solrmarc sw_index.properties (note there is custom code used not yet checked into StanfordBlacklight example in SolrMarc project) <a href="http://www.stanford.edu/people/~ndushay/code4lib2010/stanford/sw_index.properties">http://www.stanford.edu/people/~ndushay/code4lib2010/stanford/sw_index.properties</a></li>
  <li>if you want more information about our Solr index or our Marc -> Solr code, please send me an email.</li>
</ul>

Naomi says: "Jessie and I are working on getting a version of this into ProjectBlacklight, but we're not quite there yet."
