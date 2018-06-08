---
categories: []
layout: page
title: Code4lib Journal Name Vote
created: 1142370513
---
<p>Vote for the Code4lib journal name!</p>
<?php global $user; if($user->name) { ?>
<p>Drag this Bookmarklet:</p>
<p><a href="javascript:void((function(){user='<?php print $user->name; ?>';h='http://rsinger.library.gatech.edu/journalnamevote/voter.js';n=navigator;d=document;a=n.userAgent.toLowerCase();if(d.getElementById&&a.indexOf('opera')==-1){if(n.appVersion.indexOf('MSIE')!=-1&&a.indexOf('mac')!=-1){o=d.createElement('div');o.innerHTML='<script type=%22text/javascript%22 src=%22'+h+'%22><\/script>';d.body.appendChild(o)}else{e=d.createElement('script');e.setAttribute('src',h);d.body.appendChild(e)}}else{alert('Sorry, unsupported browser.');}})())">Vote!</a></p>

<p>to your browser toolbar (IE users can "Save as Bookmark").</p>

<p><a href="http://jd4v15.backpackit.com/pub/498893" target="c4l_proposals">Click on this link</a> and when the page loads, click on your bookmarklet.</p>
<?php } else { echo("<p>Please log in to participate in voting!</p>"); }?>

<p>
The proposal with the most votes wins.  You can cast as many votes as you wish, but may only vote a specific name once.
</p>
<p>
Happy voting!
</p>
