---
categories:
- conferences
- code4lib 2013
layout: page
title: Hybrid Archival Collections Using Blacklight and Hydra
created: 1354662909
---
<strong>Hybrid Archival Collections Using Blacklight and Hydra</strong>
<br/>
<p><a href="https://github.com/awead/presentations">Slide presentation</a></p>

<ul>
<li>Adam Wead, Rock and Roll Hall of Fame and Museum, awead@rockhall.org</li>
</ul>

At the Library and Archives of the Rock and Roll Hall of Fame, we use available tools such as Archivists' Toolkit to create EAD finding aids of our collections. However, managing digital content created from these materials and the born-digital content that is also part of these collections represents a significant challenge. In my presentation, I will discuss how we solve the problem of our hybrid collections by using Hydra as a digital asset manager and Blacklight as a unified presentation and discovery interface for all our materials.

Our strategy centers around indexing ead xml into Solr as multiple documents: one for each collection, and one for every series, sub-series and item contained within a collection. For discovery, we use this strategy to leverage item-level searching of archival collections alongside our traditional library content. For digital collections, we use this same technique to represent a finding aid in Hydra as a set of linked objects using RDF. New digital items are then linked to these parent objects at the collection and series level. Once this is done, the items can be exported back out to the Blacklight solr index and the digital content appears along with the rest of the items in the collection.
