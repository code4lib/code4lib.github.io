---
categories:
- code4lib 2012
layout: post
title: 'NoSQL Bibliographic Records: Implementing a Native FRBR Datastore with Redis
  - Jeremy Nelson'
created: 1327557715
permalink: /conference/2012/nelson/
---
<strong>NoSQL Bibliographic Records: Implementing a Native FRBR Datastore with Redis</strong>
<ul>
<li>Jeremy Nelson, Colorado College, jeremy.nelson@coloradocollege.edu</li>
</ul>
<p><a href="/conference/2012">code4lib 2012</a>, Wednesday, February 8 2012, 10:55-11:15</p>
<p>
In October, the Library of Congress issued a news release, "A Bibliographic Framework for the Digital Age" outlining a list of requirements for a New Bibliographic Framework Environment. Responding to this challenge, this talk will demonstrate a Redis (<a href="http://redis.io">http://redis.io</a>) FRBR datastore proof-of-concept that, with a lightweight python-based interface, can meet these requirements.
</p>
<p>
Because FRBR is an Entity-Relationship model; it is easily implemented as key-value within the primitive data structures provided by Redis. Redis' flexibility makes it easy to associate arbitrary metadata and vocabularies, like MARC, METS, VRA or MODS, with FRBR entities and inter-operate with legacy and emerging standards and practices like RDA Vocabularies and LinkedData.
</p>
