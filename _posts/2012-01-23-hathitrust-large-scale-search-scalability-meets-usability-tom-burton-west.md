---
categories:
- code4lib 2012
layout: post
title: 'HathiTrust Large Scale Search: Scalability meets Usability - Tom Burton-West'
created: 1327338930
---
<strong>HathiTrust Large Scale Search: Scalability meets Usability</strong>
<ul>
<li>Tom Burton-West, DLPS, University of Michigan Library, tburtonw AT umich edu</li>
<li><a href="http://www.hathitrust.org/documents/HathiTrust-Code4Lib-201202.pptx">Slides</a></li>
</ul>
<p><a href="/conference/2012/">code4lib 2012</a>, Tuesday 7 February 2012, 13:00-13:20</p>
<p>
<a href="http://www.hathitrust.org/">HathiTrust Large-Scale search</a> provides full-text search services over nearly 10 million full-text books using Solr for the back-end. Our index is around 5-6 TB in size and each shard contains over 3 billion unique terms due to content in over 400 languages and dirty OCR.
</p>
<p>
Searching the full-text of 10 million books often results in very large result sets. By conference time a number of <a href="http://www.hathitrust.org/full-text-search-features-and-analysis">features</a> designed to help users narrow down large result sets and to do exploratory searching will either be in production or in preparation for release. There are often trade-offs between implementing desirable user features and keeping response time reasonable in addition to the traditional search trade-offs of precision versus recall.
</p>
<p>
We will discuss various <a href="http://www.hathitrust.org/blogs/large-scale-search">scalability</a> and usability issues including:
<ul>
<li>Trade-offs between desirable user features and keeping response time reasonable and scalable</li>
<li>Our solution to providing the ability to search within the 10 million books and also search within each book</li>
<li>Migrating the <a href="http://babel.hathitrust.org/cgi/mb">personal collection builder application</a> from a separate Solr instance to an app which uses the same back-end as full-text search.</li>
<li>Design of a scalable multilingual spelling suggester</li>
<li>Providing advanced search features combining MARC metadata with OCR</li>
<li>The dismax mm and tie parameters</li>
<li>Weighting issues and tuning relevance ranking</li>
<li>Displaying only the most "relevant" facets</li>
<li>Tuning relevance ranking</li>
<li>Dirty OCR issues</li>
<li>CJK tokenizing and other multilingual issues.</li>
</ul>
</p>
