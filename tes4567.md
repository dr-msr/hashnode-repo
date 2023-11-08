---
title: "General Idea"
datePublished: Sat May 13 2023 20:04:26 GMT+0000 (Coordinated Universal Time)
cuid: clhmf1ivb000109ju42fp9d6e
slug: general-idea

---

So basically I have this one remote desktop setup, The Hub. I am intending to use it via remote desktop protocol (RDP) because of the nature of my work. I'll elaborate more on the hub series for that.

The general idea is that, that remote server is not going to be powered on 24/7. It would be too pricey. I'm glad to that the provider is using CloudVM as the virtual manager. It allows me to use their API and then using the app HTTP Shortcuts on my phone, i've written some basic code to retrieve the server status, to suspend it and to resume it.

However it seems quite rough and so inelegant. So I was imagining something like this:

A dashboard site, hosted on a serverless or free hosting. When I arrived at my workplace, I can use the PC in my workplace and assess the dashboard site. The URL would be something like https://dashboard.drmsr.dev. The database that I'll be using is from Firebase. On the dashboard I can execute a open speed test to gauge the ping and jit speed towards my remote server. Based on that I will know whether it will be comfortable for me to connect to my remote server via RDP or its going to be laggy.

The dashboard will also serve as a check-in page of my work. This will be integrated in a separate project I'm thinking of doing, maybe I'll elaborate more in a dedicated series. Basically it will create a new record, retrieve the geo location of my workplace and store it in the firebase as well. Moving forward, it may even track my hours working and other things too.

And then i'll put a API link so that i can start, stop, restart my server based on the dashboard alone. Ah, maybe i'll make it like an automated sequence : first the script will unfreeze The Hub, and then run the speedtest, and will return with results and prompt whether I want to continue connecting via RDP or suspend The Hub back.

But first, at this dashboard, i'm gonna need some access manager of course. Currently it will be me alone accessing the dashboard and I dont think I will have different people accessing it. The Hub is my workstation and there's privacy issue about it, heck, its one of the reason i'm opting for a remote desktop solution anyway.

For the authentication process, I dont want to enter username or password. I want something that is seamless. Something akin to Github login flow, where they will prompt the login code on your phone and you dont have to type anything except the login code. It looks so elegant but I want something even better.

I was thinking something like QR-code login. The process should be : Upon loading, the dashboard will display a dynamic QR code. I will scan the QR code using my phone, which will send an API request to my dashboard script alongside a security token. Only when both of them are correct, the dashboard will be unlocked. This process also will ensure that only my phone that scanned the QR Code will be allowed to continue.

Yeah to be fair its something like 2FA but i guess thats too complicated, at least for a single user like me. So it doesnt have to be tied to the clock/time. And of course i dont have to build a dedicated android app/module for that. The dashboard will just use my pre-installed token in the browser, or my device's UUID as a key. Something that is already there.

So i'm surveying into what are solutions that I can use for the QR Code login thing. Firebase comes with a great authentication module, maybe i'll look into it. I found one tech service, Branches.io that provides QR-based authentication method but when I tried to register, the website fails. Oh well maybe another time i'll look into it again.

But now the basic things. So what stack i'm gonna use? I already have Firebase in hand, and as for CSS framework i think i'll use Tailwind. How about front end? I found something quite modular yesterday i forgot the name huhu. Maybe i'll just use React, i dont know.