---
categories:
- conferences
- code4lib 2013
layout: post
title: Evolving Towards a Consortium MARCR Redis Datastore
created: 1354662651
---
<strong>Evolving Towards a Consortium MARCR Redis Datastore</strong>
<br/>
<p><a href="http://tuttdemo.coloradocollege.edu/code4lib/">Slide presentation</a></p>

<ul>
<li>Jeremy Nelson, Colorado College, jeremy.nelson@coloradocollege.edu</li>
<li>Sheila Yeh, University of Denver, Sheila.Yeh@du.edu</li>
</ul>

The current state of technology in library automation is not keeping pace with the explosive growth in information storage and retrieval system. The lag costs institutions as well as users’ resource discovery. To address this problem, we should look into how successfully enterprise such as Craigslist and StackOverflow manage and scale their enormous volume of data. The key lies in the Redis, a NoSQL open source advanced key-value data structure server. Therefore, Colorado College and the University of Denver, along with the Colorado Alliance of Research Libraries are exploring and co-developing a MARCR Redis Datastore. It is a peer-to-peer bibliographic datastore, modeled using the Library of Congress Bibliographic Framework's new Linked Data based MARC 21 replacement, called MARCR (MARC Resources). The structure of MARCR leads itself to an advanced Consortium catalog where a Work is cataloged once and multiple institutions have complete control over their own Instances of the Work, de-duplicating cataloging efforts while supporting real-time resource sharing between the Instances. Control, access, and discovery of records in the proposed MARCR Redis Datastore are provided through lightweight HTML5 responsive apps built with Django, Bootstrap, and KnockoutJS that also integrate with both open-source and commercial discovery products.

Redis offers many advantages for a shared MARCR bibliographic datastore, such as speed, scalability, and ease-of-deployment. Especially it can support multiple cloud models that benefits institution of various size and capital. We will demonstrate a MVP (Minimal Viable Product) iteration of this MARCR Datastore using the transformed MARC 21 records from Colorado College and the University of Denver into Redis with coordination by Colorado Alliance of Research Libraries.

<video controls="" poster="https://ia601207.us.archive.org/8/items/Day2JeremyNelsonAndSheilaYeh/Day2-Jeremy%20Nelson%20and%20Sheila%20Yeh.gif"><source src="https://ia601207.us.archive.org/8/items/Day2JeremyNelsonAndSheilaYeh/Day2-Jeremy%20Nelson%20and%20Sheila%20Yeh.mp4" type="video/mp4"><source src="https://ia601207.us.archive.org/8/items/Day2JeremyNelsonAndSheilaYeh/Day2-Jeremy%20Nelson%20and%20Sheila%20Yeh.ogv" type="video/ogg"></video><p><a href="https://ia601207.us.archive.org/8/items/Day2JeremyNelsonAndSheilaYeh/Day2-Jeremy%20Nelson%20and%20Sheila%20Yeh.mp4">Download the video</a></p>
