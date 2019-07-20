---
layout: post
title: "de-Googling"
date: 2019-07-15 12:00 -0700
categories: CS
tags: CS privacy security
---

---

For as long as I've reasonably been using the internet, I've been a loyal Google customer. Naturally, it started with their search engine, but from there I have used tons of their products quite loyally: GMail (my first email client), Google Maps, Google+ (I somehow got invite early access to it back in 7th grade or so), Google Drive, Google Home, Chromecasts, using it to sync up my notes between devices, Google Calendars, Google Chrome, Android phones... the list goes on. I was perfectly content with my Google-integrated digital lifestyle; they were coming out with innovation after innovation (excuding Google+) and each new product worked so nicely with the others that the convenience was really hard to beat. Plus, they seemed like a pretty ethical company without major scandal, so I had seen no issues with entrusting so much data to them.
<br><br>
About a year ago, three things occurred that started to change my persepctive on Google, though:

1. I started reading up a lot on computer security and privacy, and decided that I enjoyed the topic enough to put serious time into trying to learn about it.
2. News had broken about Facebook's [Cambridge Analytica scandal](https://www.vox.com/policy-and-politics/2018/3/23/17151916/facebook-cambridge-analytica-trump-diagram), showing just how easy it is to mess up data privacy.
3. I started getting more into open-source software.

The combination of these three things drove me to start questioning my loyalty to Google's products. Why was it that every new thing they created I felt like I needed to use? Did they have any Facebook-esque scandals that I hadn't heard about?
<br><br>
I decided to do some digging, and sure enough, the scandals began to flow. Notable ones include [that time Google gave out access to your GMail account to third parties](https://www.independent.co.uk/life-style/gadgets-and-tech/news/google-gmail-data-sharing-email-inbox-privacy-scandal-a8548941.html), as well as the more recent Google Home/Amazon Alexa type issues.
<br><br>
<img src="https://tctechcrunch2011.files.wordpress.com/2013/05/insight-xkcd.png" alt="Me right now">
<br>
*How I imagine I'll sound by the end of this*
<br><br>
The more I researched, the more disgusted and annoyed I became. It was at that point that a phrase I had heard finally clicked for me: "*If a product is free and not open-source, it is because **you** are the product instead of the consumer*". As much as Facebook and Google (and others) try to deny it, they're essentially advertising companies selling their services (read: your data) to corporations. Just stop and think about the business model of IKEA compared to Google compared to Apple compared to Workday, and this becomes painstakingly clear.
<br><br>
At this point, I had decided that I had had enough. I was gonna "de-Google". For full disclosure, it's been about half a year since I've embarked on this endeavour and I still have a long way to go, but it's certainly a start.
<br><br>
I'll now start going through the products I've been taking myself off of and what I've been replacing them with, as well as other suggested alternatives; a full list of alternatives can be found [here](https://www.techspot.com/news/80729-complete-list-alternatives-all-google-products.html).

* **Google search**: This was an easy one. I switched from Google to [DuckDuckGo](https://duckduckgo.com) a while ago and haven't really looked back since. If nothing else, I *highly* recommend switching to this over Google due to the commitment to privacy and security expressed by the DuckDuckGo team.

* **GMail**: This one was a tough one to leave, since it integrates fully with other services such as YouTube. I've been using [ProtonMail](https://protonmail.com), and though it isn't free, the end-to-end encryption, built in PGP client, and extra features like how it safeguards from phishing makes it a much better choice on the whole.

* **Google Chrome**: This was another hard one to leave due to how convenient Chrome is, but due to things like [Google planning to remove the ability to block adverts](https://mspoweruser.com/google-is-planning-to-remove-ad-blockers-from-chrome-and-it-might-be-time-to-look-for-alternatives/), and [Google silently making Chrome automatically sign you into your account, even if you didn't want to be signed in](https://news.ycombinator.com/item?id=17942252), I had finally had enough. I've since switched to [Brave browser](https://brave.com/), a free, open-source, Chromium based alternative that has better privacy settings, built in adblock, access to the Chrome WebStore (for extensions), and even features the ability to open windows connecting to the [Tor network](https://www.torproject.org/) make it a great choice for me. Other fantastic alternatives include [Firefox by Mozilla](https://www.mozilla.org/en-US/firefox/new/). On mobile, I recommend either Firefox, DuckDuckGo's browser (this is the option I picked), or [Aloha Browser](https://alohabrowser.com/). 

* **Google Maps**: Unfortunately, this one is hard to get rid of. Due to pretty lacklustre competition *cough Apple Maps cough*, I stil use Google Maps a decent amount. However, in supported cities, I've been using a combination of [OneBusAway](https://onebusaway.org/) and [CityMapper](https://citymapper.com) to get around instead.

* **Google+**: Well this one was [yeeted by Google recently partially due to security issues](https://www.cnet.com/news/google-reportedly-exposed-data-of-hundreds-of-thousands-of-google-users/), so no need to worry about this one.

* **Google Drive**: This one has been *really* tough to leave, since my personal Drive has a lot of space and my school Drive account has **TONS** of space to use. Once I leave school, my plan is to get myself a Raspberry Pi, hook it up to a 2TB SSD, then use it as a way to remotely sync things in my own sort of cloud storage solution. Some other options include [Sync](https://www.sync.com/pricing/), [syncthing](https://github.com/syncthing/syncthing/tree/master), or [ownCloud if you prefer hosting it yourself](https://owncloud.org/).

* **Google Docs**: Once I hook up my filehosting solution, I'll migrate from this back to [OpenOffice](https://www.openoffice.org/) or even Microsoft Word, but for now, I'm stuck here on Docs.

* **Google Home/Chromecasts**: Google Home has no good replacements (Alexa is just as bad), so I've been using it less and less with plans on just removing it. Chromecast has been really useful, and with no scandals (for now), it remains a Google product I can actually endorse. Regarding scandals, Google Home has had [their fair share](https://www.independent.co.uk/life-style/gadgets-and-tech/news/google-home-smart-speaker-audio-recordings-privacy-voice-spy-a9000616.html) and honestly, the convenience of it really doesn't justify the reports.

* **Android Phones**: This one saddens me; I truly believe Android OS is a superior phone operating system compared to iOS, but I am just not okay with letting Google get so much information about me via my phone. I'm sticking with iPhones solely because Apple's core business model revolves around selling overpriced, aesthetically pleasing devices instead of selling data.

* **Google Calendar**: My email client, ProtonMail, is beta testing their own encrypted calendar service. Once this is released, I'll be switching off of Google Calendar completely.

* **Google Keep**: For synching notes between devices with encryption, I've been using [Joplin](https://joplinapp.org/) and I haven't regretted it. Markdown, end-to-end encryption, fully featured mobile app and desktop app *and* terminal app makes it a no-brainer choice.

* **YouTube**: Though not a "replacement", per se, an option is to use Invidio. Simply replace the portion of the URL that reads `youtube.com` with `invidio.us` and you're good to go.

* **Google Translate**: On desktop, [DeepL](https://www.deepl.com/translator) is a great choice, but if you want a cross-platform experience then check out [Linguee](https://www.linguee.com/). Both function really well, like Translate, but without Google.

* **Google's Password Manager**: There are plenty of paid options (like LastPass and Dashlane), but I've been sticking to a free, open-source alternative called [Bitwarden](https://bitwarden.com/) and it's been great so far.

* _**Bonus: Messaging Apps**_: Facebook Messenger (in secure mode) is actually surprisingly good, but IMO the best option for secure messaging is to use [Signal](https://www.signal.org/). It's free, open-source, and makes use of the signal protocol for end-to-end encryption to ensure privacy and security on conversations (even group chats, though it does have a few issues with those).

<br><br>
I still have a lot of work to do in this area, but I would encourage those reading to begin de-Googling themselves a bit more as well. At the minimum, switch your search engine to DuckDuckGo and maybe switch browsers to Firefox. Maybe a full de-Google isn't right for you, but I believe it's high time to start taking back a bit more control over our data and how it is collected and used.

---
[Go back](/innermachinations)
