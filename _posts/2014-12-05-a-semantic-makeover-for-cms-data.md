---
categories: []
layout: post
title: A Semantic Makeover for CMS Data
created: 1417818966
---
- Bill Levay, @wjlevay, wjlevay@gmail.com, Linked Jazz Project, Code4Lib first-timer

How can we take semi-structured but messy metadata from a repository like CONTENTdm and transform it into rich linked data? Working with metadata from Tulane’s Hogan Jazz Archive Photography Collection, the Linked Jazz Project used Open Refine and Python scripts to tease out proper names, match them with name authority URIs, and specify FOAF relationships between musicians who appear together in photographs. Additional RDF triples were created for any dates associated with the photos, and for those images with place information we employed GeoNames URIs. Historical images and data that were siloed can now interact with other datasets, like Linked Jazz’s rich set of names and personal relationships, and can be visualized ([see prototype visualization](http://linkedjazz.org/tulane/)) or otherwise presented on the web in any number of ways.

GitHub: [https://github.com/wjlevay/tulane-jazz-data](https://github.com/wjlevay/tulane-jazz-data)

Presentation Slides: [download via Dropbox](https://dl.dropboxusercontent.com/u/42852848/levay-code4lib-slides.pdf)
