---
excerpt: "<p>Vote for the Code4lib 2006 presentations!</p>\r\n<?php global $user;
  if($user->name) { ?>\r\n<p>Drag this Bookmarklet:</p>\r\n<p><a href=\"javascript:void((function(){user='<?php
  print $user->name; ?>';h='http://rsinger.library.gatech.edu/code4libvoter/voter.js';n=navigator;d=document;a=n.userAgent.toLowerCase();if(d.getElementById&&a.indexOf('opera')==-1){if(n.appVersion.indexOf('MSIE')!=-1&&a.indexOf('mac')!=-1){o=d.createElement('div');o.innerHTML='<script
  type=%22text/javascript%22 src=%22'+h+'%22><\\/script>';d.body.appendChild(o)}else{e=d.createElement('script');e.setAttribute('src',h);d.body.appendChild(e)}}else{alert('Sorry,
  unsupported browser.');}})())\">Vote!</a></p>\r\n\r\n<p>to your browser toolbar
  (IE users can \"Save as Bookmark\").</p>\r\n\r\n<p><a href=\"http://inkcow.backpackit.com/pub/354440\"
  target=\"c4l_proposals\">Click on this link</a> and when the page loads, click on
  your bookmarklet.</p>\r\n<?php } else { echo(\"<p>Please log in to participate in
  voting!</p>\"); }?>\r\n<p>You may choose up to 11 proposals.</p>\r\n\r\n<p>Voting
  closes at January 9th 11PM EST.</p>\r\n<p>\r\nThe 11 proposals with the most votes
  win.  In case of a tie, we will have a \"run off\" election tomorrow, January 10th
  at 5PM - 11PM EST.\r\n</p>\r\n<p>\r\nI will be deleting all votes cast before 5PM
  EST unless you specifically tell me that you have to vote early.  So, be sure to
  tell me.  Seriously.  Send an email to ross.singer@library.gatech.edu.  \r\n</p>\r\n<p>\r\nHappy
  voting!\r\n</p>"
categories:
- conferences
- code4lib 2006
layout: post
title: Voting on Code4Lib 2006 Presentation Proposals
created: 1136581781
---
<p>Vote for the Code4lib 2006 presentations!</p>
<?php global $user; if($user->name) { ?>
<p>Drag this Bookmarklet:</p>
<p><a href="javascript:void((function(){user='<?php print $user->name; ?>';h='http://rsinger.library.gatech.edu/code4libvoter/voter.js';n=navigator;d=document;a=n.userAgent.toLowerCase();if(d.getElementById&&a.indexOf('opera')==-1){if(n.appVersion.indexOf('MSIE')!=-1&&a.indexOf('mac')!=-1){o=d.createElement('div');o.innerHTML='<script type=%22text/javascript%22 src=%22'+h+'%22><\/script>';d.body.appendChild(o)}else{e=d.createElement('script');e.setAttribute('src',h);d.body.appendChild(e)}}else{alert('Sorry, unsupported browser.');}})())">Vote!</a></p>

<p>to your browser toolbar (IE users can "Save as Bookmark").</p>

<p><a href="http://inkcow.backpackit.com/pub/354440" target="c4l_proposals">Click on this link</a> and when the page loads, click on your bookmarklet.</p>
<?php } else { echo("<p>Please log in to participate in voting!</p>"); }?>
<p>You may choose up to 11 proposals.</p>

<p>Voting closes at January 9th 11PM EST.</p>
<p>
The 11 proposals with the most votes win.  In case of a tie, we will have a "run off" election tomorrow, January 10th at 5PM - 11PM EST.
</p>
<p>
I will be deleting all votes cast before 5PM EST unless you specifically tell me that you have to vote early.  So, be sure to tell me.  Seriously.  Send an email to ross.singer@library.gatech.edu.  
</p>
<p>
Happy voting!
</p>
