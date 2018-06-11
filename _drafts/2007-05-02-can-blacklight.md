---
excerpt: "Feedback from a <a href=\"http://aleph.lib.virginia.edu/blacklight\" target=\"_blank\">Blacklight</a>
  user during its 2-week trial period:\r\n\r\n<blockquote>\r\nBut can it also enable
  users to execute targeted multi-faceted searches directly?\r\n\r\nFor example, it
  is impossible with the <a href=\"https://virgo.lib.virginia.edu/uhtbin/cgisirsi/KuTpujP1qC/UVA-LIB/146110125/60/1180/X\">current
  Virgo</a> to perform the following search of the following type which our users
  would find useful: \"retrieve all of the printed works in special collections relating
  to the Civil War that were published in New York between 1861-1863.\"  This search
  is impossible for general users to precisely target because they are not given the
  ability to search publication location directly even under the advanced search options.\r"
categories: []
layout: blog
title: Can Blacklight... ?
created: 1178113324
---
Feedback from a <a href="http://aleph.lib.virginia.edu/blacklight" target="_blank">Blacklight</a> user during its 2-week trial period:

<blockquote>
But can it also enable users to execute targeted multi-faceted searches directly?

For example, it is impossible with the <a href="https://virgo.lib.virginia.edu/uhtbin/cgisirsi/KuTpujP1qC/UVA-LIB/146110125/60/1180/X">current Virgo</a> to perform the following search of the following type which our users would find useful: "retrieve all of the printed works in special collections relating to the Civil War that were published in New York between 1861-1863."  This search is impossible for general users to precisely target because they are not given the ability to search publication location directly even under the advanced search options.

Can or will Blacklight be able to support these types of multi- faceted direct searches that involve, potentially, the full array of MARC fields?
</blockquote>

Well, sort of.

My response was this:

<blockquote>
As for the full array of MARC fields, one interesting point about Blacklight is that the entire MARC string (as shown in the detail page of a particular resource if you click "toggle raw MARC display") is indexed into the full-text search too. This means that any text there (within limits of the analysis process) is full-text searchable, for example song titles that aren't specifically/ individually made searchable.

I've just hopped over to the the LOC MARC descriptions and see the publication information is in the 260 field. Currently the Blacklight indexer is extracting years from 260$c, but we are not pulling 260$a specifically (but again, the entire MARC text is indexed so all is not lost). For example, here's a set of constraints that might get you pretty close to what you're after:

<code>
 + "new york"
 + "civil war"
 + year_facet:[1861 TO 1863]
 + library: SPEC-COLL
</code>

First I selected SPEC-COLL from the library facet, then full-text searched for "new york" (with quotes to get it as a phrase), then added another full-text search for "civil war", and then finally I used fielded search on the year (called year_facet in the index, so this is not very user friendly yet) using <a href="http://www.lucenebook.com/search?query=query+parser+syntax" target="_blank">Lucene query syntax</a> for the year range of 1861-1863. There are 112 matches for those criteria, making it possible to see all of those documents in 4 clicks of the "next page" arrow.

Are we getting warmer?
</blockquote>

And it looks like this: <img src="http://code4lib.org/files/spec-coll.png"/>

Now the big question is, where do we go now with this glorious hack I call Blacklight?

The feedback has been overwhelmingly positive both internally and externally, thanks to <a href="http://www.ibiblio.org/bess/?p=75">Bess</a>, <a href="http://www.patacriticism.org/collex/2007/04/11/spotlight-on-blacklight/">Bethany</a>, and even <a href="http://orweblog.oclc.org/archives/001341.html">Lorcan Dempsey</a> publicizing our efforts. Several times I've written elaborate colorful blog entries about Blacklight... in my head. After the code4lib conference I put life on hold a bit while I implemented Blacklight from the Solr Flare pieces, helped Bess & co. deploy it, and babysat it a bit. I'm finally coming out of the dark now about it because we've had a chance to prove the technologies and even the usability of the system to staff internally and surely to many institutions around the world who are actively looking to improve the findability experience to their users.

But we're not done! The Blacklight experience has shed light on some difficult issues facing libraries. There are a lot of big scary financial decisions involved in running a top-notch library. And facing those decisions, a prepackaged solution (open source or not) which at first glance satisfies most of our users' checklist of must-have features seems very appealing.
However, when I open up the <strong>conversation</strong> with users, I'm finding that the features they really want aren't present in <em>any</em> existing project or product. What's needed is a process, not a product. 

<strong>Making beautiful music together</strong>
Beautiful folks at the <a href="http://www.lib.virginia.edu/MusicLib/">UVa Music Library</a> provided the most elaborate feedback on Blacklight.

<blockquote>
... faceted searching is absolutely essential to the successful retrieval of muscial works.
</blockquote>

Another said:
<blockquote>
For obvious reasons, performers want to find materials scored for certain combinations of instruments and/or voices. Luckily, for many scores and recordings, the MARC 048 field is populated with specific information on the medium of performance. Sadly, we have no way to retrieve on this field at present and we really need one. The LCSH fields can sometimes be this precise, but very often cannot. For example, the 048 field for an edition of Bach’s Cantata 45 shows that it’s scored for alto, tenor, bass, 4-part mixed choir and piano: vc01 vd01 vf01 ca04 ka01 while the subject heading reads only Cantatas, Sacred—Vocal scores with piano.
</blockquote>

and similar details for dates of composition, places of recording, and language:

<blockquote>
We need to be able to retrieve on the coded data in the fixed field for language and the 041 field. While the fixed field is limited to one code, we are scrupulous about putting all sorts of data on the language of the item into the 041: it’s encoded for original language, language of translation, language of text (libretto), language of program notes (for CD), to name a few. Users are interested in locating materials based on a particular language (finding an English translation of an opera or choral work is one obvious example).
</blockquote>

Again, "all is not lost". In fact, even just dumbly indexing a #to_s on a ruby-marc MARC record does alright on <a href="http://aleph.lib.virginia.edu/blacklight/search?q=vf01+ka01">finding works with bass and piano</a> at least. Of course we'd all rather click on "Bass" and "Piano". Can Blackli... yes, with some work put into descriptive mappings and an indexer tweak to extract those fields into their own facet. Engineering estimate (rounded up to the nearest hour): 1 hour to adjust and test the indexer mapping; 1 hour to kick start a new indexer. (wait many hours at this point, the dark side of blacklight we don't talk about much ;) 1 hour (ok, I can't even justify this as a full hour), 5 minutes to add and test the addition of facet to Blacklights hardcoded list. [folks that have seen Solr Flare - we hardcoded them in a more desirable order than the auto-facet-field-detect Flare has by default, otherwise this step would have been simply "hit refresh in your browser"]

That's not all there is to it to make the Music Librarians smile though. And putting all of those facets on the overarching University library web site or the institution web site is overload to users. Specialized and branded user interfaces for select sets (err, <a href="http://www.nines.org/permalink/list/tag/lighthouse/erikhatcher">collex</a>ions anyone?) of resources is the desire I'm distilling from the Blacklight feedback. [I can't help but toss out some techie mumbo jumbo here, the enthusiasm is too overwhelming to hold back - this involves mapping a bit of the Blacklight URL space to subset defining rules/constraints and custom templates - gimme a few days and I'll knock this one out].

<strong>Sets of turtles, all the way down</strong>
But back to the more generalized UI at the parent library or institution, designed for broader sets of users, there are broader sets of facets shown. Progressive UI refinement, if you will.

Even with custom user interfaces tied to subsets, we're still not done. That's just the catalog. Our libraries are MUCH richer than the catalog. MUCH! Here at UVa we have the <a href="http://lib.virginia.edu/digital/collections/">digital collections</a>, <a href="http://etext.lib.virginia.edu/collections/">electronic texts</a>, and a slew of other <a href="http://www.lib.virginia.edu/collections.html">collections</a> including our marvelous not-so <a href="http://www.lib.virginia.edu/small/collections/overview.html">Small Special Collections Library collections</a>. The Blacklight system already includes an example of one of our cool <a href="http://aleph.lib.virginia.edu/blacklight/search?q=source_facet:tang">e-text resources</a> (to show internationalized characters working, and as a proof of concept of non-catalog data sources); in fact this custom data set even has some custom facets like type of poem that we don't expose yet.

And the needs of our users are MUCH more interactive and stateful than just search and find through a custom UI. We (hey, I'm a user too here!) want to be able to <em>use</em> those objects we discover in our information foraging. What do we want to do with objects? Well, first thing we want to do is not lose them again, so we add them to our own collections. Web 2.0 fanatics call this tagging. Call it what you will, we want to file objects away somewhere easy to retrieve later using whatever filing system we want. Heck, let's even annotate those objects a bit with some notes along the way.

Are we there yet? Are we there yet? Are we there yet? No! We also want to be able to repurpose those objects in other contexts, be it scholarly publishing, creating an annotated bibliography for your students, a slideshow for a presentation, and on and on. Can Blacklight help us here? Not yet, but Blacklight wants to grow up to be like his big sister Collex. Collex already sports user collections via tagging/annotating. I rather enjoy pronouncing Collex like "collects". (I can see Beth cringing as she reads that) However, the "ex" of Collex stems from "exhibit" by design. Over the summer we'll have some exhibit building capabilities emerge into production (it's already kinda sorta working apparently) allowing users to drag and drop resources that they have collected or that they have just discovered into customizable templates, starting with "annotated bibliography".

<strong>A decent proposal</strong>
I'm being asked what it will take for the University of Virginia Library to go into production with Blacklight as its findability user interface. Many see what we've done so far and wonder why it's not already the user interface for our catalog. I've intentionally shown, above, a couple of feature requests and my engineering estimate to accomplish them. This gives a sense of the simplicity of how it's architected to be cleanly malleable. Let me reiterate that what I see needed is a process, not a product. With Solr in the picture, we can all rest a bit easier knowing that a top-notch open source search engine is readily available... a commodity. The investment for the University of Virginia, then, is not in search engine technology per se, but rather in embracing the needs of the users at a fine-grained level. I, as a user, don't want least common denominator solutions, I want the greatest focused tailored-for-me experience I can have in using the rich resources of our libraries.

<strong>The library within a networked environment</strong>
I attended a <a href="http://orweblog.oclc.org/archives/001341.html">talk by Lorcan Dempsey</a> recently. He said some poignant things, such as <cite>users want content, not a website</cite>. One of his diagrams stood out to me, an overlapping set of 4 circles, labeled "discover", "gather", "share", and "create". He could have just been describing the philosophy we've been espousing with our little ol' Collex project for a couple of years now.

A difficult topic that is cropping up is how WorldCat Local plays along with Blacklight. To be honest, I really don't know yet. Is it an either/or question? I don't think so. To me it makes a lot of sense to communally share and improve bibliographic records, rather than every institution keeping the dusty old ones to themselves. It makes a lot of sense to allow users to tap into a broader "local" area to get physical books from nearby libraries and see the global network of reviews, uses / citations of works, and it also makes a lot of sense for us to share books with our neighbors LibraryThang "swap this book"-like.

Blacklight to me fits in as the necessary interface into the vast and rich resources individual libraries possess, bringing in data from external subscription services such as journal archives and potentially WorldCat Local's forthcoming data services, etc. It's beyond the scope of these other services to provide nuanced user interface tweaks to every sub-library of their clients, and it's beyond the scope of these services to provide integration with every custom archive, e-text center, and digital repository at each institution. In other words, you simply cannot buy the solution we want off the shelf, nor can a single subscription service give you everything you need. The local library knows the community and tailors its collections accordingly, bringing in the best, not necessarily the localest. Locality doesn't matter to a user of a music  library that has clickable MP3's (custom podcast subscriptions, anyone?).  Locality does matter to a user checking out a couple of videos for the weekend (netflix-style queuing from a collexion faceted to what's available <em>right now</em> was an idea I heard tossed out recently).

[authors prerogative: removed last misplaced bit about what I want out of Blacklight]
