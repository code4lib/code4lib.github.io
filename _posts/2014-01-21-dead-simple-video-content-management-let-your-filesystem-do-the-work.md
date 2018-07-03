---
excerpt: "Andreas Orphanides, NCSU Libraries\r\n\r\nContent management is hard. To
  keep all the moving parts in order, and to maintain a layer of separation between
  the system and content creators (who are frequently not technical experts), we typically
  turn to content management systems like Drupal. But even Drupal and its kin require
  significant overhead and present a not inconsiderable learning curve for nontechnical
  users.\r\n\r\nIn some contexts it's possible -- and desirable -- to manage content
  in a more streamlined, lightweight way, with a minimum of fuss and technical infrastructure.
  In this presentation I'll share a simple MVC-like architecture for managing video
  content for playback on the web, which uses a combination of Apache's mod_rewrite
  module and your server's filesystem structure to provide an automated approach to
  video content management that's easy to implement and provides a low barrier to
  content updates: friendly to content creators and technology implementors alike.
  Even better, the basic method is HTML5-friendly, and can be integrated into your
  favorite content management system if you've got permissions for creating templates.\r\n\r"
categories:
- conferences
- code4lib 2014
layout: post
title: 'Dead-simple Video Content Management: Let Your Filesystem Do The Work'
created: 1390336013
---
Andreas Orphanides, NCSU Libraries

Content management is hard. To keep all the moving parts in order, and to maintain a layer of separation between the system and content creators (who are frequently not technical experts), we typically turn to content management systems like Drupal. But even Drupal and its kin require significant overhead and present a not inconsiderable learning curve for nontechnical users.

In some contexts it's possible -- and desirable -- to manage content in a more streamlined, lightweight way, with a minimum of fuss and technical infrastructure. In this presentation I'll share a simple MVC-like architecture for managing video content for playback on the web, which uses a combination of Apache's mod_rewrite module and your server's filesystem structure to provide an automated approach to video content management that's easy to implement and provides a low barrier to content updates: friendly to content creators and technology implementors alike. Even better, the basic method is HTML5-friendly, and can be integrated into your favorite content management system if you've got permissions for creating templates.

In the presentation I'll go into detail about the system structure and logic required to implement this approach. I'll detail the benefits and limitations of the system, as well as the challenges I encountered in developing its implementation. Audience members should come away with sufficient background to implement a similar system on their own servers. Implementation documentation and genericized code will also be shared, as available.
