---
excerpt: "<strong>Citation search in SOLR and second-order operators</strong>\r\n\r\n<ul>\r\n<li>Roman
  Chyla, Astrophysics Data System, roman.chyla AT (cfa.harvad.edu|gmail.com)</li>\r\n</ul>\r\n\r\nCitation
  search is basically about connections (Is the paper read by a friend of mine more
  important than others? Get me a paper read by somebody who cites many papers/is
  cited by many papers?), but the implementation of the citation search is surprisingly
  useful in many other areas.\r\n\r\nI will show 'guts' of the new citation search
  for astrophysics, it is generic and can be applied recursively to any Lucene query.
  Some people would call it a second-order operation because it works with the results
  of the previous (search) function. The talk will see technical details of the special
  query class, its collectors, how to add a new search operator and how to influence
  relevance scores. Then you can type with me: friends_of(friends_of(cited_for(keyword:\"black
  holes\") AND keyword:\"red dwarf\"))\r\n\r"
categories:
- conferences
- code4lib 2013
layout: page
title: Citation search in SOLR and second-order operators
created: 1354662799
---
<strong>Citation search in SOLR and second-order operators</strong>

<ul>
<li>Roman Chyla, Astrophysics Data System, roman.chyla AT (cfa.harvad.edu|gmail.com)</li>
</ul>

Citation search is basically about connections (Is the paper read by a friend of mine more important than others? Get me a paper read by somebody who cites many papers/is cited by many papers?), but the implementation of the citation search is surprisingly useful in many other areas.

I will show 'guts' of the new citation search for astrophysics, it is generic and can be applied recursively to any Lucene query. Some people would call it a second-order operation because it works with the results of the previous (search) function. The talk will see technical details of the special query class, its collectors, how to add a new search operator and how to influence relevance scores. Then you can type with me: friends_of(friends_of(cited_for(keyword:"black holes") AND keyword:"red dwarf"))

<video controls="" poster="https://ia801608.us.archive.org/10/items/Day2RomanChyla/Day2-Roman%20Chyla.gif"><source src="https://ia801608.us.archive.org/10/items/Day2RomanChyla/Day2-Roman%20Chyla.mp4" type="video/mp4"><source src="https://ia801608.us.archive.org/10/items/Day2RomanChyla/Day2-Roman%20Chyla.ogv" type="video/ogg"></video><p><a href="https://ia801608.us.archive.org/10/items/Day2RomanChyla/Day2-Roman%20Chyla.mp4">Download the video</a></p>
