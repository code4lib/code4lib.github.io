---
categories: []
layout: page
title: So you want to start a Kindle lending program
created: 1323903061
---
<p><strong>Update:</strong> With the introduction of Whispercast, the ability to register a device from the Amazon website using a serial number has been removed.  It pretty much takes the best part of the following process and throws it in the trash.  Bummer.</p>

<p><em>This article is about Kindle ebook readers.  The actual hardware Kindles and not the iOS app, Android app, web reader, or Kindle Fire.  Just the good old Kindle hardware reader.  Yes, I understand there are countless ebook reader platforms and DRM free ebook collections to choose from, but if you&#8217;ve read past the title you probably understand that I&#8217;m going to focus on Kindles and content purchased from Amazon.  I appreciate your understanding.</em></p>

<p>Lending out Kindles to patrons may, on the surface, seem like a really easy thing to do and undoubtedly there is a lot of excitement with regards to using &#8220;technology&#8221; in the library.  Perhaps it&#8217;s easier to get funding for a project if you sprinkle in a little technology.  I&#8217;m not here to stomp your newfound excitement into the ground, but I do want to help you understand the technical issues that you will need to deal with to make this program workable and sustainable.  It should be noted that Kindles are designed to be personal devices and we&#8217;re using them for institutional purposes.  We are bending them about as far as they can bend without breaking.  </p>

<p>The issues around how to circulate your Kindles is beyond the scope of this article, although I will do my best to describe how our system works.  I would strongly advise that you work with your circulation folks to figure out what will work best for them with regard to these devices.</p>

<h2 id="where_to_start">Where To Start</h2>

<p>We start at the beginning, the <a href="http://www.amazon.com/gp/help/customer/display.html?nodeId=200506200">Kindle License Agreement and Terms of Use</a>.  Some very specific things that you need to know:</p>

<ul>
<li><strong>&#8220;Digital Content is licensed, not sold, to you by the Content Provider.&#8221;</strong> <br />
I&#8217;m sure this isn&#8217;t news to most of you, but it&#8217;s an important thing to know.  Kindle books are not like books in stacks.  Yes, they are both made of words, but that&#8217;s pretty much where the similarities end &#8212; for better or worse.</li>
<li><strong>&#8220;&#8230;you may not bypass, modify, defeat, or circumvent security features that protect the Digital Content.&#8221;</strong> <br />
That&#8217;s right, we&#8217;re talking about the <a href="http://en.wikipedia.org/wiki/Digital_Millennium_Copyright_Act">DMCA</a>.  So, don&#8217;t try and root your Kindle or strip the DRM off those ebooks.</li>
<li><strong>&#8220;In order to keep your Software up-to-date, Amazon may automatically provide your Kindle or Other Device with updates/upgrades to the Software.&#8221;</strong> <br />
Unless of course you keep them completely off the network, which also renders them somewhat less functional.</li>
</ul>

<p>Another very important piece of information is tucked away at the bottom of this <a href="http://www.amazon.com/gp/help/customer/display.html/ref=hp_kip_faq_num?nodeId=200298470&amp;#howmany">Kindle Help</a> page, which is that you can use up to 6 Kindle devices to access the ebooks purchased from a single Amazon account.  Basically that means you will need a separate Amazon account for every six Kindles.  That also means that if you want an ebook on, say, 12 Kindles, you would need to purchase the ebook in both accounts.  But, you&#8217;re thinking big.  You want to buy <strong>one-hundred</strong> Kindles.</p>

<p><strong>100/6 = 17 accounts</strong> (you can&#8217;t have 16.6 accounts, you have to round up)</p>

<p>But no matter how many Kindles you plan on buying, you will want to keep some critical pieces of information about each device in a place that is accessible by the people who will manage them.  You will want to keep a list/spreadsheet/database current with the name (Kindle 1, etc.), serial number, and MAC address.  The MAC address will be handy if your organization has the ability to whitelist devices for Wi-Fi access.</p>

<h2 id="the_good_old_days_of_managing_a_kindle_collection">The Good Old Days Of Managing A Kindle Collection</h2>

<p>So, you have your 6 or 100 Kindles and you&#8217;re ready to start buying books.  How do you get from buying books on amazon.com to having them on all your Kindles?  Well, that <em>used</em> to be a lot easier.  I realize that it&#8217;s a bit mean of me to tell you how good things used to be and that you can&#8217;t have those nice things, but I think highlighting how frustrating DRM is for customers is important.  Feel free to skip ahead a bit, I won&#8217;t; think less of you.  It turns out that prior to Kindle firmware 3.3 you could take Kindle books off a Kindle device and load them onto other devices and it would &#8220;just work.&#8221;  Yes, even content purchased from different Amazon accounts.  It was the best thing ever in terms of dealing with purchased content for your Kindles.  You could use software, such as Calibre, to manage a central collection of ebooks.  The easy way to get a Kindle ready for check-out was to reset to factory defaults and then use Calibre to copy your collection to the Kindle via the USB cable.  From blank slate to full of ebooks in 5 minutes.  You could do this without even registering the Kindle!  It was truly a glorious way to deal with Kindles.</p>

<p>But then 3.3 hit and now each ebook is tied to a specific device, most likely by the serial number required when you register the device.  There is no (safe) way to downgrade your Kindle, and even if you could as soon as it got on a Wi-Fi network, it would upgrade itself.  The days of having a centralized Kindle library are over.</p>

<h2 id="the_new_reality_of_managing_a_kindle_collection">The New Reality Of Managing A Kindle Collection</h2>

<p>If you&#8217;re managing Kindles you simply have to maintain a library (essentially a backup of the books on the device that you store on your computer) for each Kindle.  Luckily there is <a href="http://calibre-ebook.com/">Calibre</a>, which has very nice support for Kindles and maintaining multiple libraries.  Calibre is like an open source iTunes for ebooks.  It can manage all your files and synchronize them with devices like the Kindle.  If you are going to have multiple people managing Kindles, make sure you create your Calibre libraries on a file server that these folks all have access to from their desktops.  </p>

<p>The easiest way to seed each library is to register the Kindle and download all your ebooks from the Kindle <em>Archived Items</em>.  The Kindle <em>Archived Items</em> is where you can retrieve purchased books from Amazon that are not currently on the device, assuming that the device is registered with the purchasing account of course.  You&#8217;ll see <em>Archived Items</em> listed on the main screen when the device is registered with an account.  The end game is that you have downloaded all the books to the device so that we can back them all up using Calibre.  Yes, this is tedious and annoying, but it only has to be done once.  That is, until we get to buying new content.</p>

<p>To back up the books after they have all been downloaded, open Calibre and create a new library on your network share, preferably named after the Kindle you are using (we use &#8216;Kindle 1&#8217; though &#8216;Kindle 6&#8217;).  Once all your ebooks are on the device, plug your Kindle in via USB and use Calibre to transfer all the books to the library for that Kindle.  You now have a &#8220;pristine&#8221; library <em>for that particular Kindle</em>.  Thanks to the DRM on the ebooks you will need to repeat this for <strong>every</strong> Kindle.</p>

<p>After you have a library for a Kindle, you can deregister the device and reset it to factory defaults.</p>

<ol>
<li>From the Kindle Home screen, hit Menu and select Settings.</li>
<li>Once in Settings, hit Menu again and select &#8220;Reset to Factory Defaults.&#8221;</li>
</ol>

<p>Now you can restore content from the library without having to register the device (the DRM seems to be tied to the serial number).</p>

<ol>
<li>Launch the Calibre software and select the proper library for the Kindle you&#8217;re working with.</li>
<li>Connect Kindle to the PC via the USB cable, wait until the Kindle displays that it is in USB Drive Mode and the Kindle Device icon appears on the Calibre toolbar.</li>
<li>Click the Library icon in the toolbar and then select all the ebooks in Calibre library.</li>
<li>Send all Kindle ebooks the device by clicking the Send to Device icon.</li>
<li>From the Device icon, select Eject Device.</li>
</ol>

<p>The advantages to this model is that you can have almost anyone manage a Kindle without them having to know anything about the account that was used to purchase the content.  Care must be taken to make sure that you sync the right library with the right Kindle, otherwise, the content will be unreadable.</p>

<h2 id="adding_content_to_your_kindle_libraries">Adding Content To Your Kindle Libraries</h2>

<p>Now that we&#8217;ve made &#8220;pristine&#8221; copies of each Kindle, what happens when you buy a book?  Well, this part will be a bit of work as well.  As you know, the Kindle DRM is now more strictly enforced, so a copy will need to be procured for each device.  You can do this from the Kindle itself, but it will need to be registered first (once registered purchased ebooks will appear in <em>Archived Items</em>) and that can be rather time consuming, especially depending on how many Kindles you have.  After you download the ebook to the Kindle you will want to transfer that ebook into the Calibre library for that Kindle.  You can also download Kindle files from the Amazon web site and place those in the Calibre library, but you must do that for <em>each</em> device.  When you register a device on the Amazon web site (aren&#8217;t you glad you have that list of serial numbers?), the device itself will be registered, assuming that it has network access.  At that point, the device could make purchases on the account.  Conversely, when you register the device from the Kindle, it will show up in your list of devices on the Amazon web site.</p>

<p>This can make getting copies of an ebook into your Calibre libraries (a unique copy of every ebook for every Kindle, it&#8217;s the DRM way) tricky, especially if you&#8217;re registering a Kindle that it is currently checked out by a patron.  If the patron has registered the Kindle under their own account and then you try to register the device on the Amazon web site, you will receive an error message stating that the Kindle cannot be registered.  This is probably a good thing in terms of the patron experience.</p>

<h2 id="the_reality_of_kindles">The Reality of Kindles</h2>

<p>Previously I said that Kindles were personal devices.  What did I mean by that?  Kindles are designed to be owned by a single person with an Amazon account.  They are not loaned out to &#8220;friends&#8221; (or in our case, patrons).  You don&#8217;t worry about somebody else using your Kindle because, well, it&#8217;s <em>yours</em>.  Why would somebody else even have it in the first place?  The only &#8220;control&#8221; you can place on access to the device is a simple password.  Once you are past that, access is unfettered, and by &#8220;unfettered&#8221; I mean that 1-Click™ purchasing is now available.  Again, the device isn&#8217;t designed to be used for institutional purposes.  In fact, it&#8217;s not even designed to be used for familial purposes.  Many people are used to, or at least familiar with, the idea that any device can have certain features disabled unless a passcode is provided.  Remember when the <a href="http://transition.fcc.gov/vchip/">V-Chip</a> was a thing?  Yeah, neither does anyone else, but parental controls are something that are expected of major operating systems.  Mac OS, iOS, and Windows all have features that allow the device to be crippled for users who don&#8217;t know that magic incantation to unlock all the levels.  The Kindle has none of this.  You can&#8217;t restrict network access.  You can&#8217;t restrict purchases.  In fact, here is the text from the Amazon site:</p>

<blockquote>
  <p>"All Kindle transactions are completed with 1-Click. Changes made to your default 1-Click method will apply to future Amazon.com 1-Click transactions, but will not change your current active subscriptions."</p>
</blockquote>

<p>This is why Kindles <em>must</em> be unregistered before they are sent out the door.  Well, unless you have an unlimited budget, of course.  At the beginning I mentioned that the Kindle Fire was excluded from this discussion.  Why?  Well, it turns out that a Fire is pretty much useless unless it&#8217;s registered with an Amazon account, and yes, the lack of &#8220;parental controls&#8221; extends to the Fire.</p>

<h2 id="circulating_your_kindles">Circulating Your Kindles</h2>

<p>Again, I can&#8217;t stress enough that you will want to work closely with the folks that run circulation to make sure you come up with a workable plan.  I will ignore the details of our catalog, which will undoubtedly differ from yours in more ways than they are similar.  Our system is fairly basic: the patron either places a hold on a Kindle from the web interface of the catalog or can request a Kindle from our main circulation desk.  The Kindles have bar codes on the front, along with a name tag for easy visual identification.  The Kindles all have cases that hold the charger cord and two laminated cards, one with the &#8220;rules&#8221; and the other with a quick &#8220;cheat sheet&#8221; for navigating the Kindle.  Kindles must be checked in at the main circulation desk to a real person.  There is a replacement fee for returning a Kindle in a non-working condition (actually broken, not just a dead battery).</p>

<h2 id="in_summary">In Summary</h2>

<p>There is a lot to managing a small number of Kindles and thanks to DRM the process does not scale well.  The start up costs, in terms of creating the initial libraries, are somewhat high and the on-going maintenance of keeping the libraries up to date as you purchase more ebooks is certainly non-trivial.  That being said, it <em>can</em> be done.  So, depending on how badly you need to be able to lend Kindles, you may want to rethink your plans.  There are certainly scenarios where the work involved would be justified by the benefit to the patron or perhaps in cost savings.</p>

<p>If you have any questions, comments, suggestions, or complaints please feel free to contact me.</p>

<p>Patrick Berry - <a href="mailto:pberry@csuchico.edu">pberry@csuchico.edu</a> - CSU, Chico</p>
