---
excerpt: "There was a session at code4lib 2006 on using IM bots to deliver library
  services.  I was at a different session, but I thought about it a bit and realized
  that the \"jake-like\" queries to the CUFTS database could fairly easily be adapted
  to the IM world.  \"jake-like\" queries being \"where is this journal indexed?\",
  \"where is there fulltext for this journal and what's the coverage\", etc.  I started
  on a quick bot while I was there, got that working and finished up a fairly comprehensive
  version last week.\r\n\r\nConnecting the bot to the IM network was very easy thanks
  to Net::OSCAR.  Unfortunately, it doesn't include file transfers, but everything
  else I wanted was there.  Since I already had the database and queries mostly written,
  the bulk of the work was formatting the results for IM size display, handling \"more\"
  commands, and writing help.\r"
categories:
- perl
- code4lib 2006
layout: page
title: CUFTS2 AIM/AOL/ICQ bot
created: 1141083107
---
There was a session at code4lib 2006 on using IM bots to deliver library services.  I was at a different session, but I thought about it a bit and realized that the "jake-like" queries to the CUFTS database could fairly easily be adapted to the IM world.  "jake-like" queries being "where is this journal indexed?", "where is there fulltext for this journal and what's the coverage", etc.  I started on a quick bot while I was there, got that working and finished up a fairly comprehensive version last week.

Connecting the bot to the IM network was very easy thanks to Net::OSCAR.  Unfortunately, it doesn't include file transfers, but everything else I wanted was there.  Since I already had the database and queries mostly written, the bulk of the work was formatting the results for IM size display, handling "more" commands, and writing help.

So, you can now add "CUFTS2" as a contact on AOL/AIM/ICQ (they're all on the OSCAR network) and send it queries.  Here's an example transcript.

> help

This bot is used to search the CUFTS journals database for information on where journals are indexed, available in fulltext, and what the coverage periods are.
"help commands" will give a list of valid commands.
Example Usage:
 search outlook
 select 4
 coverage
 results
 site BVAS
 urls 2

> search american journal of b

1: American Journal of Biochemistry and Biotechnology [1553-3468]
2: American Journal of Bioethics [1536-0075, 1526-5161]
3: American Journal of Bioethics
4: American Journal of Botany [0032-0919, 0002-9122]

> select 2

Current selection: 2: American Journal of Bioethics

> full

Academic Search Alumni Edition - EBSCO
  citation: 2001-01-01 - 
Academic Search Premier - EBSCO
  fulltext: 2001-01-01 - 
  citation: 2001-01-01 - 
Biomedical Reference Collection: Comprehensive - EBSCO
  fulltext: 2001-01-01 - 
  citation: 2001-01-01 - 
Biomedical Reference Collection: Corporate - EBSCO
  fulltext: 2001-01-01 - 
  citation: 2001-01-01 - 
CINAHL - EBSCO
  No coverage information available.

( more )

> more

INAHL Plus with Fulltext - EBSCO
  No coverage information available.
CINAHL with Fulltext - EBSCO
  No coverage information available.
EBSCO Electronic Journal Service - EBSCO
  fulltext: 2001-09-01 (v.1 i.1) - 2005-09-30 (v.5 i.5)
EBSCO MegaFILE - EBSCO
  fulltext: 2001-01-01 - 
  citation: 2001-01-01 - 
Expanded Academic ASAP (with Ingenta) - Gale
  citation: 2001-01-01 - 
InfoTracâ„¢ OneFile (with Ingenta) - Gale

( more )


> site BVAS

Current site is: Simon Fraser University

> current

Current selection: 2: American Journal of Bioethics

> urls

Project Muse Standard - Project Muse
journal: http://proxy.lib.sfu.ca/login?url=http://muse.jhu.edu/journals/american_journal_of_bioethics
Taylor and Francis - MetaPress
journal: http://proxy.lib.sfu.ca/login?url=http://taylorandfrancis.metapress.com/openurl.asp?genre=journal&issn=15265161

> urls 1 open

Directory of Open Access Journals - DOAJ
journal: http://www.scipub.us/c4p.php?j_id=ajbb

> coverage 1

Directory of Open Access Journals - DOAJ
     fulltext: 2005-01-01 - 

> titles 1

American Journal of Biochemistry and Biotechnology

> titles

American Journal of Bioethics
The American Journal of Bioethics
American journal of bioethics

> search outlook

1: OUT-LOOK [0896-7733]
2: Outlook [0273-835X]
3: Outlook [0834-0242]
4: Outlook
5: Outlook [1206-033X]
6: Outlook (14993627) [1499-3627]
7: Outlook - Medical Post
8: Outlook / Department of the Solicitor General of Canada [1201-9496]
9: Outlook on Agriculture [0030-7270]
10: Outlook on Science Policy [1471-5473, 0165-0262]
11: Outlook, The
12: Outlooks on Pest Management [1743-1034, 1743-1026]
13: Outlooks on Pest Management

> search exact outlook

1: OUT-LOOK [0896-7733]
2: Outlook [0273-835X]
3: Outlook [0834-0242]
4: Outlook
5: Outlook [1206-033X]

> search Tourism Management

1: Tourism Management [0261-5177]

> marc 1

LDR 00307     2200109   4500
022    _a02615177
245 00 _aTourism management. --
246 00 _aTourism Management
650  0 _aTourism
      _xPeriodicals.
780 00 _tInternational journal of tourism management
      _x0143-2516
260 00 _aGuildford, U.K. :
      _bButterworths,
050 0  _aG155.A1


...

* Note that the "site" command only works if you're a current CUFTS site (COPPUL and ELN sites right now).
