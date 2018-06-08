---
excerpt: "In looking for a solution to organize  a local elementary school library,
  <a href=\"http://www.delicious-monster.com/\">Delicious Library</a> was my first
  stop.  And perhaps my last... except for faceting it with <a href=\"http://wiki.apache.org/solr/Flare\">Flare</a>,
  of course.\r\n\r\nI scanned a few books into Delicious Library: \r\n<img width=550
  src=\"http://www.code4lib.org/files/delicious_library.png\"/>\r\n\r\nAnd then I
  exported the library (to a tab-delimited format), wrote a little <a href=\"http://svn.apache.org/repos/asf/lucene/solr/trunk/client/ruby/solrb/examples/delicious_library/dl_importer.rb\">Delicious
  Library export -> Solr importer script</a>, and my Delicious Library is now faceted
  with Flare:\r"
categories:
- ruby
- code4lib 2007
layout: blog
title: Delicious!  Flare + SIMILE Exhibit
created: 1170570191
---
In looking for a solution to organize  a local elementary school library, <a href="http://www.delicious-monster.com/">Delicious Library</a> was my first stop.  And perhaps my last... except for faceting it with <a href="http://wiki.apache.org/solr/Flare">Flare</a>, of course.

I scanned a few books into Delicious Library: 
<img width=550 src="http://www.code4lib.org/files/delicious_library.png"/>

And then I exported the library (to a tab-delimited format), wrote a little <a href="http://svn.apache.org/repos/asf/lucene/solr/trunk/client/ruby/solrb/examples/delicious_library/dl_importer.rb">Delicious Library export -> Solr importer script</a>, and my Delicious Library is now faceted with Flare:
<img width=550 src="http://www.code4lib.org/files/flare.jpg"/>
What you see in the Flare screenshot is a filter already applied for the Grammar genre, and the Ajax term look-up drop down of me pausing after having typed "lang".

Thanks go to David Walker for letting me borrow some CSS to kick start an improved look for Flare, though the ugly bits of the look are my own doing.  The UI will only improve from here.

But wait, that's not all.  Like everyone else, I'm fascinated by the work going on at <a href="http://simile.mit.edu">SIMILE</a> (*waves to <a href="http://www.betaversion.org/~stefano/">Stefano</a> & David).  One of their many cool tools is <a href="http://simile.mit.edu/exhibit/">Exhibit</a> (not to be confused with the vastly different upcoming Collex Exhibit builder).  It could not have been easier to tie Simile's Exhibit into Flare:

<img width=550 src="http://www.code4lib.org/files/flare_simile.jpg"/>

All it took to tie the two together was to follow the <a href="http://simile.mit.edu/wiki/Exhibit/Getting_Started_Tutorial">Exhibit Getting Started tutorial</a>, which simply involved copying and pasting the HTML template, adding in the facet names to be shown, and pointing the JSON link to a tiny Rails controller I added to Flare:
<code>
class SimileController < ApplicationController
  def exhibit
    req = .... # Details of constructing the Solr request omitted, refactoring is guaranteed.
    @data = SOLR.send(req)
    
    # Exhibit seems to require a label attribute to be happy
    @data.each {|d| d['label'] = d['title_text']}
    
    respond_to do |format| 
      format.html # renders exhibit.rhtml 
      format.json { render :json => {'items' => @data}.to_json } # Exhibit seems to require data to be in a 'items' Hash
    end                                         
  end
end
</code>

The Exhibit facets entirely client-side, and as such it only gets the data given the already selected constraints of the main Flare browse interface (and also limited to the first 10 rows from Solr implicitly).  

Now we're cooking!

[Delicious Library developers note: please add smart shelves, just like every other Mac OS X app currently has.  I want all my signed books, for example, on a virtual shelf.]
