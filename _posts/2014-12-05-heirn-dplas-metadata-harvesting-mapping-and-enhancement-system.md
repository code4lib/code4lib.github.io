---
categories: []
layout: post
title: 'Heiðrún: DPLA''s Metadata Harvesting, Mapping and Enhancement System'
created: 1417819266
---
- Audrey Altman, audrey at dp.la, Digital Public Library of America
- Gretchen Gueguen, gretchen at dp.la, Digital Public Library of
America
- Mark Breedlove, mb at dp.la, Digital Public Library of America
- [Slides](https://docs.google.com/a/dp.la/presentation/d/1nsyuaKsyv8AQ6xrrQ2MSXfPJhExY3caIyJrALneoMEY/edit) and [more info](http://bit.ly/heidrun)

The Digital Public Library of America aggregates metadata for over 8
million objects from more than 24 direct partners, or Hubs, using its
Metadata Application Profile (MAP), an RDF metadata application profile
based on the Europeana Data Model. After working with the initial system
for harvesting, mapping and enhancing our Hub’s metadata for a year, we
realized that it was inadequate for working with data at this scale.
There were architectural issues; it was opaque to non-developer and
partner staff; there were inadequate tools for quality assurance and
analysis; and the system was unaware that it was working with RDF data.
As the network of Hubs expanded and we ingested more metadata, it became
harder and harder to know when or why a harvest, a mapping task, or an
enrichment went wrong because the tools for quality assurance were
largely inadequate.

The DPLA Content and Technology teams decided to develop a new system
from the ground up to address those problems. Development of Heidrun,
the internal version of the new system, started in October 2014.
Heidrun’s goals are to make it easier for us to harvest and map metadata
from various sources and in variety of schemas to the DPLA MAP, to
better enrich that metadata using external data sources, and to actively
involve our partners in the ingestion process through access to better
QA tools. Heidrun and its componentry are built on Ruby on Rails,
Blacklight, and ActiveTriples. Our presentation will give some
background on our design principles and processes used during
development, the architecture of the system, and its functionality. We
plan to release a version of Heidrun and its components as a generalized
metadata aggregation system for use by DPLA Hubs and others working to
aggregate cultural heritage metadata.
