---
excerpt: "<a href=\"http://www.nabble.com/INTERNET-ARCHIVE-goes-SOLR%21-tf3129097.html#a8670095\"><em>\"INTERNET
  ARCHIVE goes SOLR\"</em></a> reports <a href=\"http://www.archive.org/~tracey\">Tracey
  Jaquith</a>.  Tracey's announcement is worth quoting in its entirety:\r\n\r\n<blockquote>\r\nWe
  converted from a badly deteriorating \"home grown\" server that \r\n  was made up
  of java + jetty ( + rsync for replication) + an older \r\n  version of lucene. \r\n
  \ I make some comparisons of SOLR vs. \"prior\" using \"[]\" notes below. \r\n\r\n
  \ I parsed 2 days worth of SOLR logs to determine: \r\n    Max queries/sec: 8.8
  \r\n    Avg queries/sec: 5.4 \r"
categories: []
layout: blog
title: Attention all planets of the Solr federation
created: 1170133093
---
<a href="http://www.nabble.com/INTERNET-ARCHIVE-goes-SOLR%21-tf3129097.html#a8670095"><em>"INTERNET ARCHIVE goes SOLR"</em></a> reports <a href="http://www.archive.org/~tracey">Tracey Jaquith</a>.  Tracey's announcement is worth quoting in its entirety:

<blockquote>
We converted from a badly deteriorating "home grown" server that 
  was made up of java + jetty ( + rsync for replication) + an older 
  version of lucene. 
  I make some comparisons of SOLR vs. "prior" using "[]" notes below. 

  I parsed 2 days worth of SOLR logs to determine: 
    Max queries/sec: 8.8 
    Avg queries/sec: 5.4 
    Number (re)indexed / day: 3372 

  Index size: 1.1gb [vs. 26gb] 
  Number of document fields searched on a quoted unqualified query: 
    5 [vs. 677] * 

  Horsepower: 
    one 4gb RAM dual core cpu 
    [vs. three 4gb RAM dual core cpu (readers) and one 8gb RAM 2 dual 
core cpus (writer)] 

  Solr hardly touches our disks, load avg stays around 0.5, typically. 
  "sar" shows we average 85% idle! 
  Solr seems quicker to respond, overall, and much more stable. 
  We can reindex our entire set of 575K items in about 2 hours 
     (where we are limited more by the "crawling" of our 190 servers for 
XML than Solr). 

  With our current configuration, we can show index changes on our live 
site in < 15 minutes 
  (compared to our last SE which could take 4+ hours) 
  Related to above point, we commit every 15 minutes; we optimize 
once/day late at night. 

  * To be fair, Michael StAck (our greatest help for prior SE "life 
support") 
  has smartly pointed out that by making a smarter schema and strategy, 
I could 
  reduce the number of fields searched from 677 to 5, with the same overall 
  functionality.  677 fields search on most queries was surely part of 
bucket 
  of nails in the coffin of our prior SE. 


  [Some information and configuration] 

  We've done essentially no optimizing outside of focusing on a "smart" 
schema. 
  We do query-time boosting (more on that follows). 
  We (presently) do not use replication. 
  We do (server-side) XSLT of output into our prior SE's XML format. 
  We don't use DisMax and (as of now) do not use faceting. 
  We override defaultOperator of "OR" to "AND". 
  We increased our commitLockTimeout to 5 minutes, and unlockOnStartup. 
  We useCompoundFile (for the index). 
  External to Solr, we use XSLT to transform our item XML into a 
post-able form for Solr to (re)index. 

  And finally, the hardest part to convert to Solr. 
  I had to write a PHP front-end custom converter to take our query strings, 
  parse the clauses and lucene syntax into pieces, and "expand" clauses 
where 
  they were not searching a specific field to expand it to our 
query-time boosting. 
  Eg: if someone were to look for "tracey pooh" on our site, we expand 
it to: 
  (title:"tracey pooh"^100 OR description:"tracey pooh"^15 OR 
collection:"tracey pooh"^10 OR language:"tracey pooh"^10 OR text:"tracey 
pooh"^1) 
  (but 'creator:"tracey pooh"' would pass to SOLR as is). 
  
  Lastly, a feelgood. All of Internet Archive's written code is opensource, 
  as is *all* the third-party code we use! 
  So go SOLR and thank you SO much for keeping it open, keeping it real, 
and for *saving our site*! 
  Thanks for the great mail list and all the continual work, updating, 
and thinking the Solr 
  team continues to do.  We have all been greatly impressed by this 
project and it has worked out 
  better than we had hoped!
</blockquote>
