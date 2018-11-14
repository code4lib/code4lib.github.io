---
excerpt: "<strong><i>n</i> Characters in Search of an Author</strong>\r\n<ul>\r\n<li>Jay
  Luker, IT Specialist, Smithsonian Astrophysics Data System, jluker@cfa.harvard.edu</li>\r\n</ul>\r\n\r\nWhen
  it comes to author names the disconnect between our metadata and what a user might
  enter into a search box presents challenges when trying to maximize both precision
  and recall [0]. When indexing a paper written by \"Wäterwheels, A\" a goal should
  be to preserve as much as possible the original information. However, users searching
  by author name may frequently omit the diaeresis and search for simply, \"Waterwheels\".
  The reverse of this scenario is also possible, i.e., your decrepit metadata contains
  only the ASCII, \"Supybot, Zoia\", whereas the user enters, \"Supybot, Zóia\". If
  recall is your highest priority the simple solution is to always downgrade to ASCII
  when indexing and querying. However this strategy sacrifices precision, as you will
  be unable to provide an \"exact\" search, necessary in cases where \"Hacker, J\"
  and \"Häcker, J\" really are two distinct authors.\r\n\r"
categories:
- conferences
- code4lib 2013
layout: post
title: n Characters in Search of an Author
created: 1354662505
---
<strong><i>n</i> Characters in Search of an Author</strong>
<ul>
<li>Jay Luker, IT Specialist, Smithsonian Astrophysics Data System, jluker@cfa.harvard.edu</li>
</ul>

When it comes to author names the disconnect between our metadata and what a user might enter into a search box presents challenges when trying to maximize both precision and recall [0]. When indexing a paper written by "Wäterwheels, A" a goal should be to preserve as much as possible the original information. However, users searching by author name may frequently omit the diaeresis and search for simply, "Waterwheels". The reverse of this scenario is also possible, i.e., your decrepit metadata contains only the ASCII, "Supybot, Zoia", whereas the user enters, "Supybot, Zóia". If recall is your highest priority the simple solution is to always downgrade to ASCII when indexing and querying. However this strategy sacrifices precision, as you will be unable to provide an "exact" search, necessary in cases where "Hacker, J" and "Häcker, J" really are two distinct authors.

This talk will describe the strategy ADS[1] has devised for addressing common and edge-case problems faced when dealing with author name indexing and searching. I will cover the approach we devised to not only the transliteration issue described above, but also how we deal with author initials vs. full first and/or middle names, authors who have published under different forms of their name, authors who change their names (wha? people get married?!). Our implementation relies on Solr/Lucene[2], but my goal is an 80/20 mix of high- vs. low-level details to keep things both useful and stackgnostic [3].

[0] <a href="http://en.wikipedia.org/wiki/Precision_and_recall">http://en.wikipedia.org/wiki/Precision_and_recall</a> 
[1] <a href="http://www.adsabs.harvard.edu/">http://www.adsabs.harvard.edu/</a> 
[2] <a href="http://lucene.apache.org/solr/">http://lucene.apache.org/solr/</a> 
[3] <a href="http://en.wikipedia.org/wiki/Portmanteau">http://en.wikipedia.org/wiki/Portmanteau</a>
