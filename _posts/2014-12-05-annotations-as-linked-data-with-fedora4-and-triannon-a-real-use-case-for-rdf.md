---
categories:
- code4lib 2015
layout: page
title: Annotations as Linked Data with Fedora4 and Triannon (a Real Use Case for RDF!)
created: 1417819277
---
- Rob Sanderson, azaroth@stanford.edu, Stanford University Libraries
- Naomi Dushay, ndushay@stanford.edu, Stanford University Libraries

Annotations on content resources allow users to contribute knowledge
within the digital repository space. W3C Open Annotation provides a
comprehensive model for web annotation on all types of content, using
Linked Data as a fundamental framework. Annotation clients generate
instances of this model, typically using a JSON serialization, but need
to store that data somewhere using a standard interaction pattern so
that best of breed clients, servers, and data can be mixed and matched.

Stanford is using Fedora4 for managing Open Annotations, via a
middleware component called Triannon. Triannon receives the JSON data
from the annotation client, and uses the Linked Data Platform API
implementation in Fedora4 to create, retrieve, update and delete the
constituent resources. Triannon could be easily modified to use other
LDP implementations, or could be modified to work with linked data other
than annotations.

**Slides:**
[http://www.slideshare.net/azaroth42/annotations-as-linked-data-with-fedora4-and-triannon](http://www.slideshare.net/azaroth42/annotations-as-linked-data-with-fedora4-and-triannon)

**Code:**

[https://github.com/sul-dlss/triannon](https://github.com/sul-dlss/triannon)  ( rails engine gem)  
[https://github.com/sul-dlss/triannon-service](https://github.com/sul-dlss/triannon-service)  (rails app using triannon)  
[https://github.com/ld4l/open_annotation_rdf](https://github.com/ld4l/open_annotation_rdf)  (active triples model gem)  
[https://github.com/ActiveTriples/ActiveTriples](https://github.com/ActiveTriples/ActiveTriples)  (active triples gem)  
[https://github.com/ruby-rdf/linkeddata](https://github.com/ruby-rdf/linkeddata)  (all teh RDF gems)  
[https://github.com/ruby-rdf/rdf](https://github.com/ruby-rdf/rdf)  (core rdf gem)  
RDF vocabs:  
[https://github.com/sul-dlss/rdf-open_annotation](https://github.com/sul-dlss/rdf-open_annotation)  
[https://github.com/sul-dlss/rdf-ldp](https://github.com/sul-dlss/rdf-ldp)  
[https://github.com/sul-dlss/rdf-iiif](https://github.com/sul-dlss/rdf-iiif)  
[https://github.com/sul-dlss/rdf-fcrepo4](https://github.com/sul-dlss/rdf-fcrepo4)  

**Specifications:**

[http://www.openannotation.org/spec/core/](http://www.openannotation.org/spec/core/) (Open Annotation)
[http://www.w3.org/TR/annotation-model/](http://www.w3.org/TR/annotation-model/) (Annotation draft towards W3C technical recommendation)
[http://iiif.io/api/presentation/2/](http://iiif.io/api/presentation/2/) (IIIF Presentation API)
[http://www.w3.org/TR/ldp](http://www.w3.org/TR/ldp) (Linked Data Platform API)
[http://www.w3.org/TR/json-ld/](http://www.w3.org/TR/json-ld/) (JSON-LD)
