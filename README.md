# Twitter-PlanB

So as you may or may not know Twitter was bought by Elon Musk, it was assumed things would take a few weeks or months to shake out. In the first week, he fired several top execs including the one responsible for safety, and content moderation on the platform. It's now (2022-11-04) one-week after, and Elon Musk has just fired roughly half of Twitter's global workforce including several entire teams. Elon Musk has also stated that Twitter needs to find 1 Billion per year in infrastructure savings, which is sadly possible if Twitter gets rid of extra capacity needed to service big events like national elections or natural disasters. There are also reports that advertisers are bailing out on Twitter and that advanced ad sales for 2023 basically hit a brick wall, so it is unclear at this point how much this will snowball in the next 3-6 months. Maybe Twitter survives, and maybe it goes bankrupt.

In other words, Twitter went from boring to highly risky. You can start dealing with this risk now, or leave it until you MUST deal with it. At the rate things have gone in the first week I'm not sure how much time we have.

# Alternatives to Twitter

There are alternative social networks, but none fall into the unique category of micro-blogging/commenting/replies that Twitter occupies. Because Twitter is primarily text-based (with support for images and video) the cost and speed to create high-quality content are very low, and people with small follower counts have posted polls and memes that do incredibly well (tens of thousands to millions of interactions). 

Platforms like YouTube, TikTok, Instagram, Pinterest, and so on are primarily video and image focussed and do not generally drive the types of conversations and interactions that happen on Twitter. Platforms like Signal, WeChat, Telegram, Discord, Slack, and so on are primarily focused on the real-time conversation for smaller groups of people, and have scaling issues (not just technologically but from a human interface point of view). The legacy platforms like LinkedIn and Facebook are what they are, and if they were a realistic alternative to Twitter, why did you leave them for Twitter in the first place?

# So what do we replace Twitter with?

The only real alternative to Twitter is Mastodon, and/or staying on Twitter. I suspect many content publishers will stay on Twitter, to quote several "Twitter is huge, it drives engagement, and it is critical for my/our brand", but fortunately there is nothing to stop people or organizations from posting all their content to both Twitter and Mastodon.

# What is Mastodon

> Mastodon is free and open-source software for running self-hosted social networking services. It has microblogging features similar to the Twitter service, which are offered by a large number of independently run Mastodon nodes (technically known as instances), each with its own code of conduct, terms of service, privacy options, and moderation policies. https://en.wikipedia.org/wiki/Mastodon_(software)

# Users of Twitter

Before we get into using Mastodon, I also wanted to cover some of the problems/concerns of the various types of Twitter users.

## Regular users

A lot of people like Twitter because it lets them follow some people and read their content quickly. If the people you follow the move to Mastodon and you want to consume their content, you'll need to set up a Mastodon account and follow these people. You'll need to get used to a slightly different interface, but other than that not a lot will change. Oh, there won't be any ads, so that's nice.

## Journalists / Researchers

Many journalists and researchers use Twitter to keep an eye on things, contact people, get quotes, to ask questions, and so on. I heavily rely on Twitter for new InfoSec happenings, a great example being the timeline I did for #log4shell which includes a couple of tweets that were days in advance of the issue officially going public, had we paid attention then...

One major challenge faced by journalists on Twitter (and in general on social media platforms) is reaching out to people for quotes/questions and making sure you have the correct person. It's well known that "Fake" accounts with real names exist and would happily troll journalists. So establishing that the person you are talking to is indeed the correct person is a real challenge for these users, especially when they are on a deadline.

## People and organizations with followers

Many people and organizations use Twitter to engage with their public fans, publish information, and so on. The Cloud Security Alliance is a good example of this, our account (@cloudsa) has 17k+ followers, and virtually everything it tweets is just information about new papers, working groups, and other Cloud Security Alliance activities. This Twitter account is vital as part of the engagement funnel that brings people and organizations into the Cloud Security Alliance and gets the word out about our new work.

## Advertisers on Twitter

Advertising on Mastodon isn't really a thing, you'll need to contact people directly to do sponsorships or similar things.

# Some technical background on Mastodon (what is federation?)

Basically, Mastodon takes the same approach as DNS. You can set up a server, create accounts, and they can follow accounts on the local server or other servers by simply specifying @username@server or https://server/username/. This leads to the benefits of federation like other people with the same name can take that named account on another server, and leads to problems of federation, like other people taking the same name as you on other servers and pretending to be you.

Regardless, federation has one major advantage over centralized services like Twitter: no one entity controls it all, there are different servers with different rules and cultures, and you can move around (although that is painful, much like switching email hosting providers). You can also set up your own Mastodon server with your own DNS if you want a permanent home. 

# Joining Mastodon

https://joinmastodon.org/

# Finding and verifying people on Mastodon

You can go through your existing Twitter account followers/followed and find people with Mastodon URLs in their profiles and then add them. There are also services that will help with this:

* https://pruvisto.org/debirdify/ (slightly more search options)
* https://fedifinder.glitch.me/ 

Both appear to work and need read access to your Twitter account:

* See Tweets from your timeline (including protected Tweets) as well as your Lists and collections.
* See your Twitter profile information and account settings.
* See accounts you follow, mute, and block.

Please note that the Cloud Security Alliance does not endorse this service, but realistically doing this manually is going to be tiresome and error-prone. Burt if you do use them download the CSV files and import them into your existing Mastodon account (use merge not overwrite). 

## Check their existing social profiles

As above, the primary way to currently discover people ius to check their existing social media profiles to see if they have listed their Mastodon ID/link in them in the form @name@server or https://server/name/.

## Out-of-band verification

If you find an account on Mastodon and are unsure if it is "real" or not you can verify it using other means such as checking their other known social media accounts, their website for a link, emailing them, and so on. This has scale problems (both for validating at scale and people receiving tons of emails requesting they prove that they are who they say they are). I suspect as Mastodon takes off we will see some tools and services to aid in this (e.g. similar to previous attempts like keybase.io).

## Updating your existing social networks with your Mastodon handle

I strongly suggest you put your Mastodon name @username@service into your other social media profiles to aid discovery and verification. You can also link it, e.g. https://infosec.exchange/@kurtseifried

## Linking to your Mastodon profile

Please note that anyone can link to it, e.g. https://seifried.org/ links to Kurt Seifried's 3 main accounts (the trick is to use rel="me" in the href link), but someone could put those links on any website. Ideally, they should be correlated, e.g. "I want kurt@seifried.org, seifried.org links to accounts X/Y/Z so those must be the real ones"

# Dealing with imposters

I'm not sure how this will work, you'll need to deal with each unique Mastodon server which may or may not have abuse policies/etc to deal with this (assuming the imposter is doing anything abusive). I think the best advice right now is to simply register your name on as many servers as you can and then link them, much like how we deal with DNS squatting. It's a terrible non-solution, but I don't have anything else to offer at this time.

# Dealing with abuse on Mastodon

You will need to deal with the abuse in the context of the server it originates from, which may or may not have abuse policies or abuse handling procedures. Some information on filtering is here: https://docs.joinmastodon.org/user/moderating/ also please note if you are running a public site you should also read this article on content filtering: https://www.techdirt.com/2022/11/02/hey-elon-let-me-help-you-speed-run-the-content-moderation-learning-curve/

# Picking a Mastodon host or service

Picking a Mastodon service is a lot like picking an email host. On the one hand, any Mastodon server can communicate with any other Mastodon server, so no matter what you pick you'll be able to follow people on other services, and they'll be able to follow you. On the other hand, picking the same server that is used by the people you communicate with heavily can be more efficient and will aid in the discoverability of your content (Mastodon servers show local content primarily when browsing). There are community-specific and oriented servers, e.g. https://infosec.exchange for the InfoSec community.

## Setting up your own Mastodon server

You can use a MaaS (Mastodon-as-a-Service), a hosting provider with pre-setup images that only require configuration, or you can set it up entirely yourself.

My general comments on this after running an experimental Mastodon service: This is most suited for large organizations with a lot of people that will be using Mastodon and want to provide a controlled space where e.g. abuse can be dealt with by the organization rather than relying on an external server. So for example a large company, University, these sorts of organization might want to run its own Mastodon server. Even if an organization requires users to have a Mastodon account for work (e.g. social media-related jobs), it is easy to set up a work account on an external server. The most significant advantages of running your own Mastodon server would be:

* vanity domain
* being able to block other servers/users for all of your users
* being able to deal with abuse reports internally according to your own laws/regulations
* enforcing identity policies and naming conventions


### Mastodon-as-a-Service (MaaS)

* https://masto.host/
* https://hostdon.jp/#/
* https://federation.spacebear.ee/software/mastodon
* https://ossrox.org/store/mastodon
* https://weingaertner-it.de/

Please note that many Mastodon services are based in Germany for the simple reason that the primary company behind Mastodon, Mastodon gGmbH, is a German company. 

### Mastodon containers/etc.

* https://marketplace.digitalocean.com/apps/mastodon

### Limiting signups in Mastodon

If you want to run a Mastodon server but limit signups the easiest way to do this is specify your email domain(s) in EMAIL_DOMAIN_ALLOWLIST (https://docs.joinmastodon.org/admin/config/#email) to limit signups to email domains you control/own.

## Setting up a Mastodon server at the root of your DNS

Mastodon is a web service, so if you want to server it from yourdomain.tld you can't have a regular web server there. The good news is that you can run your existing web server at yourdomain.tld and add a file to point Mastodon clients to your actual Mastodon server, e.g. at mastodon.yourdomain.tld. For more information on this please see https://github.com/felx/mastodon-documentation/blob/master/Running-Mastodon/Serving_a_different_domain.md (TL;DR: use .well-known/ files).

## Cross posting content from Mastodon to Twitter

Many organizations and indviduals have built up significant Twitter profiles, clearly abandoning these in place would be a waste of effort. One possible strategy to use if moving to Mastodon is to continue to post content to Twitter, allowing for engagement with the postings (e.g. replies, rewtweets), but drive direct engagement (e.g. DM's, requests) to Mastodon. Several bots exist to cross post content:

* https://github.com/renatolond/mastodon-twitter-poster
* https://github.com/yogthos/mastodon-bot
* https://github.com/AmauryCarrade/MastodonToTwitter

There are also a number of Python, go, etc. libraries for Mastodon and Twitter.

# Setting up a custom account name/domain via web finger

Mastodon supports webfinger, which allows you to place a JSON text file on a web server and redirect @accoutname@domain.tld to whatever Mastodon account you want. The documentation is at https://docs.joinmastodon.org/spec/webfinger/

To setup webfinger so that @kurt@seifried.org redirects to @kurtseifried@mastodon.social you will need to create a web finger file in the ".well-known" directory at the web root, e.g., https://seifried.org/.well-known/webfinger

This needs to contain JSON data that specifies the account and where to send it:

```
{
  "subject": "acct:kurt@seifried.org",
  "aliases": [
    "https://mastodon.social/@kurtseifried",
    "https://mastodon.social/users/kurtseifried"
  ],
  "links": [
    {
      "rel": "http://webfinger.net/rel/profile-page",
      "type": "text/html",
      "href": "https://mastodon.social/@kurtseifried"
    },
    {
      "rel": "self",
      "type": "application/activity+json",
      "href": "https://mastodon.social/users/kurtseifried"
    },
    {
      "rel": "http://ostatus.org/schema/1.0/subscribe",
      "template": "https://mastodon.social/authorize_interaction?uri={uri}"
    }
  ]
}
```

TODO: update docs for multiple entries example.

# Moving social networks

I debated adding this but there are some good resources on this topic:

* https://doctorow.medium.com/how-to-leave-dying-social-media-platforms-9fc550fe5abf
