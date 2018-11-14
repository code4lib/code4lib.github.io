---
excerpt: "Martin Haye and Mark Redar, California Digital Library\r\n\r\nWeb user interfaces
  are demanding ever-more dynamism and polish, combining HTML5, AJAX, lots of CSS
  and jQuery (or ilk) to create autocomplete drop-downs, intelligent buttons, stylish
  alert dialogs, etc. How can you make automated tests for these highly complex and
  interactive UIs?\r\n\r\nPart of the answer is PhantomJS. It’s a modern WebKit browser
  that’s “headless” (meaning it has no display) that can be driven from command-line
  Selenium unit tests. PhantomJS is dead simple to install, and its blazing speed
  and server-friendliness make continuous integration testing easy. You can write
  UI unit tests in {language-of-your-choice} and run them not just in PhantomJS but
  in Firefox and Chrome, plus a zillion browser/OS combinations at places like SauceLabs,
  TestingBot and BrowserStack.\r\n\r\nIn this double-team live code talk, we’ll explain
  all that while we demonstrate the following in real time:\r\n<ul>\r\n<li>Start with
  nothing.</li>\r\n<li>Install Selenium bindings for Ruby and Python.</li>\r\n<li>In
  each language write a small test of an AJAX-y UI.</li>\r\n<li>Run the tests in Firefox,
  and fix bugs (in the test or UI) as needed.</li>\r\n<li>Install PhantomJS.</li>\r\n<li>Show
  the same tests running headless as part of a server-friendly test suite.</li>\r"
categories:
- conferences
- code4lib 2014
layout: post
title: 'PhantomJS+Selenium: Easy Automated Testing of AJAX-y UIs'
created: 1390337432
---
Martin Haye and Mark Redar, California Digital Library

Web user interfaces are demanding ever-more dynamism and polish, combining HTML5, AJAX, lots of CSS and jQuery (or ilk) to create autocomplete drop-downs, intelligent buttons, stylish alert dialogs, etc. How can you make automated tests for these highly complex and interactive UIs?

Part of the answer is PhantomJS. It’s a modern WebKit browser that’s “headless” (meaning it has no display) that can be driven from command-line Selenium unit tests. PhantomJS is dead simple to install, and its blazing speed and server-friendliness make continuous integration testing easy. You can write UI unit tests in {language-of-your-choice} and run them not just in PhantomJS but in Firefox and Chrome, plus a zillion browser/OS combinations at places like SauceLabs, TestingBot and BrowserStack.

In this double-team live code talk, we’ll explain all that while we demonstrate the following in real time:
<ul>
<li>Start with nothing.</li>
<li>Install Selenium bindings for Ruby and Python.</li>
<li>In each language write a small test of an AJAX-y UI.</li>
<li>Run the tests in Firefox, and fix bugs (in the test or UI) as needed.</li>
<li>Install PhantomJS.</li>
<li>Show the same tests running headless as part of a server-friendly test suite.</li>
<li>(Wifi permitting) Show the same tests running on a couple different browser/OS combinations on the server cloud at SauceLabs – talking through a tunnel to the local firewalled application.</li>
</ul>
