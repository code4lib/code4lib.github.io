---
categories:
- conferences
- code4lib 2013
layout: page
title: 'ARCHITECTING ScholarSphere: How We Built a Repository App That Doesn''t Feel
  Like Yet Another Janky Old Repository App'
created: 1354660782
---
<strong>ARCHITECTING ScholarSphere: How We Built a Repository App That Doesn't Feel Like Yet Another Janky Old Repository App</strong>
<br/>
<p><a href="https://docs.google.com/presentation/d/1oSyF1eA1RAR-TFjsXAK15Bv31WnR_C0X1kz6bVz7RkU/edit#slide=id.p">Slide presentation</a></p>
<ul>
<li>Dan Coughlin, Penn State University, danny@psu.edu</li>
<li>Mike Giarlo, Penn State University, michael@psu.edu</li>
</ul>

ScholarSphere is a web application that allows the Penn State research community to deposit, share, and manage its scholarly works. It is also, as some of our users and our peers have observed, a repository app that feels much more like Google Docs or GitHub than earlier-generation repository applications. ScholarSphere is built upon the Hydra framework (Fedora Commons, Solr, Blacklight, Ruby on Rails), MySQL, Redis, Resque, FITS, ImageMagick, jQuery, Bootstrap, and FontAwesome. We'll talk about techniques we used to:
<ul>
<li>eliminate Fedora-isms in the application</li>
<li>model and expose RDF metadata in ways that users find unobtrusive</li>
<li>manage permissions via a UI widget that doesn't stab you in the face</li>
<li>harvest and connect controlled vocabularies (such as LCSH) to forms</li>
<li>make URIs cool</li>
<li>keep the app snappy without venturing into the architectural labyrinth of YAGNI</li>
<li>build and queue background jobs</li>
<li>expose social features and populate activity streams</li>
<li>tie checksum verification, characterization, and version control to the UI</li>
<li>let users upload and edit multiple files at once</li>
</ul>
The application will be demonstrated; code will be shown; and we solemnly commit to showing ABSOLUTELY NO XML.
