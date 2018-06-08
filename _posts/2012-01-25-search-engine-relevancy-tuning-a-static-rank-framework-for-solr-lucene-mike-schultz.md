---
categories:
- code4lib 2012
layout: page
title: Search Engine Relevancy Tuning - A Static Rank Framework for Solr/Lucene -
  Mike Schultz
created: 1327557072
---
<strong>Search Engine Relevancy Tuning - A Static Rank Framework for Solr/Lucene</strong>
<ul>
<li>Mike Schultz, formerly Summon Search Architect, mike.schultz@gmail.com</li>
</ul
<p><a href="/conference/2012">code4lib 2012</a>, Thursday, February 9 2012, 11:40-12:00</p>
<p>
Solr/Lucene provides a lot of flexibility for adjusting relevancy scoring and improving search results. Roughly speaking there are two areas of concern: Firstly, a 'dynamic rank' calculation that is a function of the user query and document text fields. And secondly, a 'static rank' which is independent of the query and generally is a function of non-text document metadata. In this talk I will outline an easily understood, hand-tunable static rank system with a minimal number of parameters.
</p>
<p>
The obvious major feature of a search engine is to return results relevant to a user query. Perhaps less obvious is the huge role query independent document features play in achieving that. Google's PageRank is an example of a static ranking of web pages based on links and other secret sauce. In the Summon service, our 800 million documents have features like publication date, document type, citation count and Boolean features like the-article-is-peer-reviewed. These fields aren't textual and remain 'static' from query to query, but need to influence a document's relevancy score. In our search results, with all query related features being equal, we'd rather have more recent documents above older ones, Journals above Newspapers, and articles that are peer reviewed above those that are not. The static rank system I will describe achieves this and has the following features:
<ul>
<li>Query-time only calculation - nothing is baked into the index - with parameters adjustable at query time</li>
<li>The system is based on a signal metaphor where components are 'wired' together. System components allow multiplexing, amplifying, summing, tunable band-pass filtering, string-to-value-mapping all with a bare minimum of parameters.</li>
<li>An intuitive approach for mixing dynamic and static rank that is more effective than simple adding or multiplying.</li>
<li>A way of equating disparate static metadata types that leads to understandable results ordering.</li>
</ul>
</p>
