---
categories:
- metadata
- conferences
- code4lib 2006
layout: post
title: conference schedule in hCalendar
created: 1137170473
---
<a href="http://microformats.org"><img src="http://microformats.org/img/mf-lg-ora.gif" border=0 style="padding: 15px;" align="left"></a>

With a bit of <a href="http://www.textualize.com/trac/browser/code4lib/calgen.py">python</a> the code4lib 2006 <a href="/2006/schedule">schedule</a> has been encoded using the <a href="http://www.microformats.com/wiki/hcalendar">hCalendar</a> microformat. hCalendar allows you to bundle up event information so it is available downstream to machines that crawl the content, while keeping the content readable for us humans. It is really very easy to grok, and the only reason for the script was to avoid repetitive typing.

Here's what a sample event looks like in hCalendar:

<code type="html">
<dt class="vevent">
<abbr class="dtstart" title="2006-02-15T19:05:00Z">11:05</abbr>- <abbr class="dtend" title="2006-02-15T19:25:00Z">11:25</abbr> - 
<span class="summary">
<a href="http://www.code4lib.org/2006/chudnov" class="uri">
Connecting Everything with unAPI and OPA</a> - Dan Chudnov</span>
</dt>
</code>

<p><br />Which is equivalent to the ical<br /></p>

<code type="ical">
BEGIN:VEVENT
SUMMARY;LANGUAGE=en:Connecting Everything with unAPI and OPA - Dan Chudnov
DTSTART:20060215T190500Z
DTEND:20060215T192500Z
URL:http://www.code4lib.org/2006/chudnov
END:VEVENT
</code>

<p>
The page includes a 'subscribe' link (at the top) to Brian Suda's <a href="http://suda.co.uk/projects/X2V/">x2v</a>, which extracts hCalendar from a page and spits back iCal for your calendaring application to ingest.</p>

<!--break-->

