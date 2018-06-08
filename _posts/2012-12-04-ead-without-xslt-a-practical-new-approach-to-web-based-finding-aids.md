---
categories:
- conferences
- code4lib 2013
layout: page
title: 'EAD without XSLT: A Practical New Approach to Web-Based Finding Aids'
created: 1354661545
---
<strong>EAD without XSLT: A Practical New Approach to Web-Based Finding Aids</strong>
<br/>
<p><a href="http://www.slideshare.net/trevorthornton/tthornton-code4lib">Slide presentation</a></p>

<ul>
<li>Trevor Thornton, New York Public Library, trevorthornton@nypl.org</li>
</ul>

The New York Public Library is reengineering its system for delivering archival finding aids on the Web. The foundation of this system is a data management application, written in Rails, within which collections and their components are managed as associated model instances, and descriptive data is stored natively as JSON and HTML. Front-end applications interact with the back-end via a flexible API that is capable of returning any part of the description at any level. This approach provides a number of benefits over the traditional XML/XSLT approach:
<ul>
<li>Data is stored natively in the format in which it is needed by the front-end application, making rendering much faster</li>
<li>Finding aid data can be lazy-loaded via AJAX requests</li>
<li>Enables presentation of the archival description beyond the traditional finding aid structure (alternate arrangements, visualizations, etc.)</li>
<li>Links to digital assets can be maintained independently of archival description</li>
<li>Data cleanup and normalization can be accomplished during and/or after ingest of original data into the system, ensuring data quality and consistency</li>
<li>Data is stored in a schema-neutral format, enabling easy transformation into other formats as required (e.g. RDF for semantic web applications, future version(s) of EAD schema for harvesting, etc.)</li>
</ul>

In this session I will describe the architecture of this system and its data model, and discuss the challenges presented in the design process.
