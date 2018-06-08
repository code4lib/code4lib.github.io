---
categories:
- irc
layout: page
title: "#code4lib irc channel faq"
created: 1142364428
---
Like any community, the #code4lib IRC channel can be intimidating to newcomers. For those who are new to the channel, here are some answers to Frequently Asked Questions.

<!--break-->

<h3>What is IRC? How do I login to #code4lib?</h3>

Basic technical information is available <a href="http://code4lib.org/irc">here</a>.

<h3>Is the channel logged?</h3>

Not publicly, no. 

<h3>Who can I ask for help?</h3>

#code4lib has a designated group of "helpers," who can answer questions or provide support. The channel's official group contacts to Freenode are Mark Matienzo (<code>anarchivist</code>), Becky Yoose (<code>yo_bj</code>), and Ross Singer (<code>rsinger</code>); all three of them have channel operator privileges.

<h3>Who will I find on #code4lib?</h3>

There is an incomplete list of regulars <a href="http://www.code4lib.org/node/87">here</a>. This is not an official list of any kind. If you're not on it yet, feel free to add your nick, your name, and a link to your website.

<h3>What about <strike>panizzi</strike> zoia?</h3>

Zoia is a <a href="http://supybot.com/">supybot</a> who hangs out in #code4lib. To get a list of commands it understands, type <code>@list</code> (the "@" symbol tells zoia you're talking to it). Here's a quick list of the more common commands:

<dl>
<dt><code>@help</code></dt>
  <dd>Find out how to use a particular command. The correct syntax is (usually) <code>@help</code> followed by the command name, e.g. <code>@help karma</code>. You can also just ask the other people on the channel how to do something.</dd>
<dt><code>@quote</code></dt>
  <dd>Add or display quotes that have been added to zoia's quote database. Type <code>@quote add "<jeffdavis> welcome to code4lib!"</code> to add a quote, <code>@quote jeffdavis</code> to see the last quote from a specific person, or <code>@quote random</code> to see a random quote</dd>
<dt><code>@naf</code></dt>
  <dd>Look up a term in the Library of Congress authority files.</dd>
<dt><code>@ana</code></dt>
  <dd>Create an English-language anagram of the word or phrase that you enter.</dd>
<dt><code>@tunes, @alltunes, @blockparty</code></dt>
  <dd>These commands look up people's listening history on <a href="http://www.last.fm/">Last.fm</a>. <code>@tunes jeffdavis</code> displays the last song that jeffdavis listened to, <code>@alltunes jeffdavis</code> lists the last half-dozen or so songs jeffdavis listened to, and <code>@blockparty</code> lists what people in the <a href="http://www.last.fm/group/code4lib/">code4lib group on Last.fm</a> are listening to. (Go ahead and add yourself to the code4lib Last.fm group if you like. You need to type <code>@audioscrobbler add yourusername</code> to be added to the blockparty.)</dd>
<dt><code>@insult, @praise</code></dt>
  <dd>Causes zoia to insult or praise the person or thing of your choice.</dd>
<dt><code>@karma</code></dt>
  <dd>You can increase or decrease the karma for a person or thing by appending two pluses or two minuses to the person or thing's name.  For example, if you type <code>jeffdavis++</code>, my karma score will increase by 1. (You can't raise your own karma.) Type <code>@karma jeffdavis</code> to see the karma for that person/thing, or just <code>@karma</code> for the three highest and lowest karma scores.  You can only raise or lower karma by one point at a time (so <code>jeffdavis++++</code> will only raise jeffdavis' karma by one point, not two), and commenting does work (<code>jeffdavis-- # you suck!</code> works correctly, thanks to gsf's regex-fu).</dd>
<dt><code>@google</code></dt>
  <dd>Do a Google search and show the first few results in-channel.</dd>
<dt><code>@more</code></dt>
  <dd>If the results of a command are over a certain length, zoia may end his response with "more" or "2 more messages". You can use the <code>@more</code> command to display the rest of zoia's response. If you didn't give zoia the original command, add the nick of the person who did, e.g. <code>@more jeffdavis</code> (this only works for one message deep on another nick).</dd>
<dt><code>@dunno</code></dt>
  <dd>When you send zoia a message it doesn't understand (for example, if you address it as if it were a person or get the syntax of a command wrong), it responds with a random error message. You can use the <code>@dunno</code> command to add a new error message to its repertoire, e.g. <code>@dunno I don't know what you're talking about.</code></dd>
</dl>

<h3>What do people talk about in-channel?</h3>

Information technology, software development, librarianship, cultural heritage, digital repositories, the web, programming languages, cataloging, metadata standards, games, food... just about anything! The channel is informal, and a lot of off-topic socializing takes place. If you don't understand something, just ask. That goes for the techie stuff as well as the social stuff -- for many regulars, #code4lib is where they learn about all kinds of interesting technology.

<h3>What are the ground rules?</h3>

<ol>
  <li>Follow the <a href="https://github.com/code4lib/code-of-conduct/blob/master/code_of_conduct.md">Code4lib code of conduct</a>.
  <li>Respect everyone.</li>
  <li>Be sensitive of the fact that cultures, opinions and ideas of what is 
 funny or appropriate are different, and that text is a very poor medium 
for conveying humor.</li>
<li>Because this is the case, and people will be people, be quick to forgive and slow to take offense.</li>
</li>
</ol>

Aside from that, it's a bit of a free-for-all. Basically, use common sense, be respectful of others, and don't do anything that will get everyone kicked off of Freenode.

<h3>what does "++" mean?</h3>

The double-plus is used to increment someone's karma (see above, in the section about zoia).

<h3>How do you do that thing where you talk about yourself in third person?</h3>

Type <code>/me agrees</code>. This allows you to send a message like <code>***jeffdavis agrees</code> rather than literally saying "I agree".
