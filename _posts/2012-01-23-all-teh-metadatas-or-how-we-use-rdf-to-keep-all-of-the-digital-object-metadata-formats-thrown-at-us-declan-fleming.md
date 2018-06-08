---
categories:
- code4lib 2012
layout: page
title: ALL TEH METADATAS! or How we use RDF to keep all of the digital object metadata
  formats thrown at us - Declan Fleming
created: 1327338506
---
<strong>ALL TEH METADATAS! or How we use RDF to keep all of the digital object metadata formats thrown at us</strong>
<ul>
<li>Declan Fleming, University of California, San Diego, dfleming AT ucsd DING edu</li>
</ul>
<p><a href="/conference/2012/">code4lib 2012</a>, Tuesday 7 February 2012, 11:40-12:00</p>
<p>
What's the right metadata standard to use for a digital repository? There isn't just one standard that fits documents, videos, newspapers, audio files, local data, etc. And there is no standard to rule them all. So what do you do? At UC San Diego Libraries, we went down a conceptual level and attempted to hold every piece of metadata and give each holding place some context, hopefully in a common namespace. RDF has proven to be the ideal solution, and allows us to work with MODS, PREMIS, MIX, and just about anything else we've tried. It also opens up the potential for data re-use and authority control as other metadata owners start thinking about and expressing their data in the same way. I'll talk about our workflow which takes metadata from a stew of various sources (CSV dumps, spreadsheet data of varying richness, MARC data, and MODS data), normalizes them into METS by our Metadata Specialists who create an assembly plan, and then ingests them into our digital asset management system. The result is a <a href="http://dl.dropbox.com/u/6923768/Work/DAMS%20object%20rdf%20graph.png">beautiful graph</a> of RDF triples with metadata poised to be expressed as <a href="https://libraries.ucsd.edu/digital/">HTML</a>, RSS, METS, XML, and opens linked data possibilities that we are just starting to explore.
</p>
