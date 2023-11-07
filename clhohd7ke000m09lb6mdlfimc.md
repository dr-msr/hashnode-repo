---
title: "Authenticating The Hub"
datePublished: Mon May 15 2023 06:45:03 GMT+0000 (Coordinated Universal Time)
cuid: clhohd7ke000m09lb6mdlfimc
slug: authenticating-the-hub

---

So, last night was not much of a progress, I think. Although i didnt make improvement in the dashboard site, I got to spend a lot of time researching on the authentication method i want to introduce in The Hub's Dashboard.

First of all, I dont think The Hub would be something accessible to the public. I am the only person going to use that. However since it involves remote server and my resources, of course I'm gonna secure it anyway. In between those two requirements, I personally would prefer a seamless and fast experience in connecting to The Hub's Dashboard. It should be accessible from any computer, since I am not going to bring my laptop most of the time. It should not require any additional app, software or technology, compatible with all kind of OS and browsers.

I was thinking into something QR code technology - i opened the site, I quickly scan a QR code on the frontpage with my phone, and voila, the dashboard is readily available to me. So I was researching some of the QR Authentication solution, last night. I found out about the passwordless concept, and I personally think that it is going to be the way forward in the future.

One that I found out was the SQRL Authenthication. It entices me that a common protocol, away from the regular OAuth by those big giant providers all over the world (Facebook, Gmail, etc). I feel like I want to adopt that. But then, the protocol isnt really up to date. Plus, I would need to install a specific app to scan the QR.

Then I found out about maximthomas/passwordless solution. It feels quite straightforward, and the Time-based OTP (TOTP) made me feel comfortable. I already has my 2FA Authenticator on my phone hence I would think this is easy to implement. It comes with a server-side configuration, that made me spend the whole night reconfiguring my Chromebook as my workstation. I was thinking of moving away from Firebase and having a small compute engine on my Google Cloud platform. I decided to use Caddy as the webserver, its easy and quick to deploy. The passwordless solution itself, comes with a Docker instance, so I spend some time experimenting with Docker as well.

This morning as I came back to my home and lay on the bed, I thought to myself - why would I move away from Firebase? Wouldnt i want to stay in Firebase, in order to make the best out of their Firestore, and possibly my other future projects?

I googled around some solution based on the keyword Firebase Passwordless authentication, and I found out about magic.link. Now that's something creative (for me). What if, instead of me having to put up my phone, scan a QR, instead, as soon as I opened the dashboard, it automatically sent me this TOTP and I can straight away enter it into the prompt, and voila im logged in. Thats even more seamless.

Challenges - spam, of course. Maybe a button, and a captcha challenge is required. Hmm. Let's try work on it today, shall we?