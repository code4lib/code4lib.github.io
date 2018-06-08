---
categories:
- conferences
- code4lib 2006
layout: page
title: Code4lib 2006 T-Shirt design vote!
created: 1138043062
---
<p>Vote for the Code4lib 2006 t-shirt design!</p>
<?php global $user; if($user->name) { ?>
<p>Drag this Bookmarklet:</p>
<p><a href="javascript:void((function(){user='<?php print $user->name; ?>';h='http://rsinger.library.gatech.edu/imagevoter/voter.js';n=navigator;d=document;a=n.userAgent.toLowerCase();if(d.getElementById&&a.indexOf('opera')==-1){if(n.appVersion.indexOf('MSIE')!=-1&&a.indexOf('mac')!=-1){o=d.createElement('div');o.innerHTML='<script type=%22text/javascript%22 src=%22'+h+'%22><\/script>';d.body.appendChild(o)}else{e=d.createElement('script');e.setAttribute('src',h);d.body.appendChild(e)}}else{alert('Sorry, unsupported browser.');}})())">Vote!</a></p>

<p>to your browser toolbar (IE users can "Save as Bookmark").</p>

<p><a href="http://inkcow.backpackit.com/pub/421110" target="c4l_proposals">Click on this link</a> and when the page loads, click on your bookmarklet.</p>
<?php } else { echo("<p>Please log in to participate in voting!</p>"); }?>
<p>You may choose 1 design.</p>

<p>
The proposal with the most votes wins.  In case of design requirements (i.e. one color designs allowed only) the design with the most votes that fits the critera wins.
</p>
<p>
Happy voting!
</p>
