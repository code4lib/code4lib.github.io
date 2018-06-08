---
excerpt: "<strong>Matching Dirty Data – Yet Another Wheel</strong>\r\n\r\n<ul>\r\n<li>Anjanette
  Young, University of Washington Libraries, younga3 at u washington edu</li>\r\n<li>Jeff
  Sherwood, University of Washington Libraries, jeffs3 at u washington edu</li>\r\n</ul>\r\n\r\n<a
  href=\"/conference/2010/schedule\">Code4Lib 2010</a> - Tuesday, February 23 - 13:20-13:40\r\n\r"
categories:
- conferences
- code4lib 2010
layout: page
title: Matching Dirty Data – Yet Another Wheel - Anjanette Young and Jeff Sherwood
  - Code4Lib 2010
created: 1267073116
---
<strong>Matching Dirty Data – Yet Another Wheel</strong>

<ul>
<li>Anjanette Young, University of Washington Libraries, younga3 at u washington edu</li>
<li>Jeff Sherwood, University of Washington Libraries, jeffs3 at u washington edu</li>
</ul>

<a href="/conference/2010/schedule">Code4Lib 2010</a> - Tuesday, February 23 - 13:20-13:40

Regular expressions is a powerful tool to identify matching data between similar files. When one or both of these files has inconsistent data due to differing character encodings or miskeying, the use of regular expressions to find matches becomes impractically complex.

The Levenshtein distance (LD) algorithm is a basic sequence comparison technique that can be used to measure word similarity more flexibly. Employing the LD to calculate difference eliminates the need to identify and code into regex patterns all of the ways in which otherwise matching strings might be inconsistent. Instead, a similarity threshold is tuned to identify close matches while eliminating false positives.

Recently, the UW Libraries began an effort to store Electronic Theses and Dissertations (ETD) in our institutional repository which runs on DSpace. We received 6,756 PDFs along with a file of UMI-created MARC records which needed to be matched to our library's custom MARC records (60,175 records). Once matched, merged information from both records would be used to create the dublin_core.xml file needed for batch ingest into DSpace. Unfortunately, records within the MARC data had no common unique identifiers to facilitate matching. Direct matching by title or author was impractical due to slight inconsistencies in data entry. Additionally, one of the files had "flattened" characters in title and author fields to ASCII. We successfully employed LD to match records between the two files before merging them.

This talk demonstrates one method of matching sets of MARC records that lack common unique identifiers and might contain slight differences in the matching fields. It will cover basic usage of several python tools. No large stack traces, just the comfort of pure python and basic computational algorithms in a step-by-step presentation on dealing with an old library task: matching dirty data. While much literature exists on matching/merging duplicate bibliographic records, most of this literature does not specify how to accomplish the task, just reports on the efficiency of the tools used to accomplish the task, often within a larger system such as an ILS. 

<a href="http://www.slideshare.net/ghostmob/matching-dirty-data">Slides on Slideshare</a>
<a href="/files/matchingdirtydata.pdf">Presentation Slides (PDF)</a>
