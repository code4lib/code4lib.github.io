---
categories:
- irc
layout: post
title: "#code4lib irc channel faq"
permalink: /irc/faq
created: 1142364428
---

## IRC Channel FAQ

Like any community, the #code4lib IRC channel can be intimidating to newcomers. For those who are new to the channel, here are some answers to Frequently Asked Questions.

<!--break-->

### What is IRC? How do I login to #code4lib?

Basic technical information [is available here](/irc).

### Is the channel logged?

Not publicly, no.

### Who can I ask for help?

#code4lib has a designated group of "helpers," who can answer questions or provide support. The channel's official group contacts to Libera are Mark Matienzo (`anarchivist`), Becky Yoose (`yo_bj`), and Ross Singer (`rsinger`); all three of them have channel operator privileges.

### What about ~~panizzi~~ zoia?

Zoia is a [supybot](https://github.com/Supybot/Supybot) who hangs out in #code4lib. To get a list of commands it understands, type `@list` (the "@" symbol tells zoia you're talking to it). Here's a quick list of the more common commands:

#### `@help`

Find out how to use a particular command. The correct syntax is (usually) `@help` followed by the command name, e.g. `@help karma`. You can also just ask the other people on the channel how to do something.

#### `@quote`

Add or display quotes that have been added to zoia's quote database. Type `@quote add "<jeffdavis> welcome to code4lib!"` to add a quote, `@quote jeffdavis` to see the last quote from a specific person, or `@quote random` to see a random quote

#### `@naf`
  Look up a term in the Library of Congress authority files.

#### `@ana`
  Create an English-language anagram of the word or phrase that you enter.

#### `@tunes, @alltunes, @blockparty`

These commands look up people's listening history on [Last.fm](https://www.last.fm/). `@tunes jeffdavis` displays the last song that jeffdavis listened to, and `@alltunes jeffdavis` lists the last half-dozen or so songs jeffdavis listened to.

#### `@insult, @praise`

Causes zoia to insult or praise the person or thing of your choice.

#### `@karma`

You can increase or decrease the karma for a person or thing by appending two pluses or two minuses to the person or thing's name.  For example, if you type `jeffdavis++`, my karma score will increase by 1. (You can't raise your own karma.) Type `@karma jeffdavis` to see the karma for that person/thing, or just `@karma` for the three highest and lowest karma scores.  You can only raise or lower karma by one point at a time (so `jeffdavis++++` will only raise jeffdavis' karma by one point, not two), and commenting does work (`jeffdavis-- # you suck!` works correctly, thanks to gsf's regex-fu).

#### `@google`

Do a Google search and show the first few results in-channel.

#### `@more`

If the results of a command are over a certain length, zoia may end his response with "more" or "2 more messages". You can use the `@more` command to display the rest of zoia's response. If you didn't give zoia the original command, add the nick of the person who did, e.g. `@more jeffdavis` (this only works for one message deep on another nick).

#### `@dunno`

When you send zoia a message it doesn't understand (for example, if you address it as if it were a person or get the syntax of a command wrong), it responds with a random error message. You can use the `@dunno` command to add a new error message to its repertoire, e.g. `@dunno I don't know what you're talking about.`

### What do people talk about in-channel?

Information technology, software development, librarianship, cultural heritage, digital repositories, the web, programming languages, cataloging, metadata standards, games, food... just about anything! The channel is informal, and a lot of off-topic socializing takes place. If you don't understand something, just ask. That goes for the techie stuff as well as the social stuff -- for many regulars, #code4lib is where they learn about all kinds of interesting technology.

### What are the ground rules?

1. Follow the [Code4lib code of conduct](https://github.com/code4lib/code-of-conduct/blob/master/code_of_conduct.md).
2. Respect everyone.
3. Be sensitive of the fact that cultures, opinions and ideas of what is funny or appropriate are different, and that text is a very poor medium for conveying humor.
4. Because this is the case, and people will be people, be quick to forgive and slow to take offense.

Aside from that, it's a bit of a free-for-all. Basically, use common sense, be respectful of others, and don't do anything that will get everyone kicked off of Libera.

### What does "++" mean?

The double-plus is used to increment someone's karma (see above, in the section about zoia).

### How do you do that thing where you talk about yourself in third person?

Type `/me agrees`. This allows you to send a message like `***jeffdavis agrees` rather than literally saying "I agree".
