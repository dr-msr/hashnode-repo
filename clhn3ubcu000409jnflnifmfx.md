---
title: "Fire away!"
datePublished: Sun May 14 2023 07:38:41 GMT+0000 (Coordinated Universal Time)
cuid: clhn3ubcu000409jnflnifmfx
slug: fire-away

---

I manage to spend the whole night setting up the boilerplate of The Hub's Dashboard. So I decided to use Firebase as the web framework. It's straightforward and I can deploy it to their web.app subdomain immediately. Later in production mode, I can just pinpoint my domain with a CNAME record. It also integrates with Firestore and I can use this dashboard as one of the main entry points to populate my database which can be used with lots of other apps later.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684048933490/8f1885c6-37ab-4c9c-92e7-88caa54f9067.png align="center")

I decided to go with local production since I'm still struggling with Git. Maybe I need to enrol into a specific learning session about Git. I thought Git should help me if I decided on a multi-platform, simultaneous, seamless transition during coding. Hmm. We'll see about that.

Firebase makes it easy as I can just straight away working from my local directory and test/emulator as well as push/deploy. My local directory is not that big, with just basic files and a javascript library in it.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1684048980202/ebf9d79d-6726-4c56-8ab0-e9e643f4c248.png align="center")

Since it's just a single HTML site I don't exactly choose any specific front-end library. I built my HTML from scratch and add the library as needed. For the API request, I decided to go with jQuery AJAX Get Method. Since the CloudVM of The Hub returns the API request with JSON, I need to learn about handling JSON data. It will be a good exercise since later on I will be logging data into Firestore.

I am struggling with CORS, though. Apparently, the CloudVM server has a CORS rule set up which makes my development a bit messy. I read that there are a few workarounds, some legit and some are just band-aid solutions. So far I'm using a CORS-Anywhere solution and maybe today I'll set up a Heroku worker just for the sake of that. But i don't think it's a permanent solution. Maybe I gotta read more about Reverse Proxy and how to use that with Firebase. It will be a much more permanent and better solution.

For the CSS framework initially, I thought of using Tailwind.css but then I told to myself that I'm not going to need all that. This is just a single-page HTML, though. So I looked around and decided to go with Halfmoon. They got a great dashboard template that suits my need. I thought of having a draggable module would be eye candy but then I realized I'm not going to use that function, not a lot anyway. So let's just stick around with basic CSS. I do need the dashboard to be responsive because I'll be accessing it via both desktop and mobile browsers.

Looking through my codes I realize it could have been more straightforward, and minimal and there are a lot of redundant codes that could have been more streamlined. I want my dashboard to be speedy and instantaneous-like. I looked into the remix. run, a full-stack framework. The structure and the fact that the single framework can be used to handle everything from frontend to back entice me but then I realized it is quite complex and I would need to be more proficient to use it. Maybe it's the way forward, later, I'll convert my scripts into Remix.run.

I still haven't figured out on the security and Authentication process. I think today is a good day to work on that. After all, I still hardcoded my API keys in the script. Let's work on that for a few hours, okay?