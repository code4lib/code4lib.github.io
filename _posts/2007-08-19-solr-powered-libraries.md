---
excerpt: "I had the great pleasure of <a href=\"http://www.loc.gov/today/cyberlc/feature_wdesc.php?rec=4113\">presenting</a>
  at the Library of Congress recently.  I'm honored to follow in some great footsteps,
  in the same <a href=\"http://www.loc.gov/today/cyberlc/results.php?cat=8\">series</a>
  as recent and very related talks by Andrew Pace and Tim Spalding.\r\n\r\n<a href=\"http://www.loc.gov/today/cyberlc/feature_wdesc.php?rec=4113\"><img
  src=\"http://code4lib.org/files/solr_at_loc_0.jpg\"/></a>\r\n\r"
categories: []
layout: blog
title: '"Solr Powered Libraries"'
created: 1187536516
---
I had the great pleasure of <a href="http://www.loc.gov/today/cyberlc/feature_wdesc.php?rec=4113">presenting</a> at the Library of Congress recently.  I'm honored to follow in some great footsteps, in the same <a href="http://www.loc.gov/today/cyberlc/results.php?cat=8">series</a> as recent and very related talks by Andrew Pace and Tim Spalding.

<a href="http://www.loc.gov/today/cyberlc/feature_wdesc.php?rec=4113"><img src="http://code4lib.org/files/solr_at_loc_0.jpg"/></a>

My talk got off to a rocky start with the graphics on my slides not showing up in PowerPoint on Windows, lost somehow in the transfer from my Mac.  After a moment of confusion, I realized I had the PDF file handy and fired that up successfully (the way the video was edited you won't see the screwup visually though, only my dazed moment).

Several members of the Smithsonian team were there, as well as my good #code4lib pals edsu and dchud.  The Smithsonian folks have done amazing work with Solr and just released their new <a href="http://siris-collections.si.edu/search/results.jsp?q=japanese+art&image.x=18&image.y=9&start=0">Solr powered search engine</a>.

After my talk I chatted with the LoC and Smithsonian coders for a while about their Lucene and Solr projects - spectacular stuff they are doing!

<hr/>
One thing that I had meant to cover in my talk was more about our actual library integration within NINES/Collex.  We currently have a <a href="http://www.nines.org/collex/new_expression?field[content]=archive:uva_library">select subset of content from UVa's library catalog in NINES</a>, and we're currently working to bring in 19th century content from other libraries, including the Houghton Library, the Humanities Research Center, Bancroft Library, Lilly Library, Newberry Library, and the Boston Athenaeum Library.  The UVa library content came in very easily with a bridge from Blacklight <a href="http://blacklight.betech.virginia.edu/search?q=year_facet:[1776%20TO%201918]%20AND%20library_facet:SPEC-COLL">filtered to the desired set of records</a>.
