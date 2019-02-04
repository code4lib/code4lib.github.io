---
excerpt: "Birkin James Diana, Brown University\r\n\r\nIn 2007 we built a system that
  dumped certain user web-requests for books into a database for offline-processing
  triggered via cron. We wanted to make the magic happen live, but knew it would take
  too long. Thus we created, sort of accidentally, a kind of old-fashioned static
  procedural job queue.\r\n\r\nOver the years we we've been repeatedly impressed with
  how useful and robust this unintended architecture has been, and it fostered thinking
  about using real job queues in Library workflows.\r\n\r\nFast-forward to the present.
  We now are using _real_ job queueing, in production, for parts of the functioning
  of Brown Digital Repository. We've also used it for ingestion scripts, and plan
  to move more lots more code to this architecture.\r\n\r\nI'd like to share & show:\r\n\r\n<ul>\r\n<li>our
  lightweight rq/redis job queueing setup</li>\r\n<li>how using job queues can speed
  up workflows via using multiple workers</li>\r\n<li>how job queueing can make workflows
  more robust, especially by simplifying failure handling</li>\r\n<li>a way we've
  smoothly avoided race-conditions that can occur in concurrent-programming</li>\r\n<li>a
  technique for using task-processing job queues to simplify complex workflows</li>\r\n</ul>\r\n\r\nrq:
  <a href=\"http://python-rq.org\">http://python-rq.org</a>\r"
categories:
- conferences
- code4lib 2014
layout: post
title: Queue Programming -- how using job queues can make the Library coding world
  a better place
created: 1390337743
permalink: /conference/2014/diana/
---
Birkin James Diana, Brown University

In 2007 we built a system that dumped certain user web-requests for books into a database for offline-processing triggered via cron. We wanted to make the magic happen live, but knew it would take too long. Thus we created, sort of accidentally, a kind of old-fashioned static procedural job queue.

Over the years we we've been repeatedly impressed with how useful and robust this unintended architecture has been, and it fostered thinking about using real job queues in Library workflows.

Fast-forward to the present. We now are using _real_ job queueing, in production, for parts of the functioning of Brown Digital Repository. We've also used it for ingestion scripts, and plan to move more lots more code to this architecture.

I'd like to share & show:

<ul>
<li>our lightweight rq/redis job queueing setup</li>
<li>how using job queues can speed up workflows via using multiple workers</li>
<li>how job queueing can make workflows more robust, especially by simplifying failure handling</li>
<li>a way we've smoothly avoided race-conditions that can occur in concurrent-programming</li>
<li>a technique for using task-processing job queues to simplify complex workflows</li>
</ul>

rq: <a href="http://python-rq.org">http://python-rq.org</a>
redis (python): <a href="https://pypi.python.org/pypi/redis/">https://pypi.python.org/pypi/redis/</a>
