---
title: "Syncing Hashnode to Wordpress.com"
datePublished: Wed Nov 08 2023 03:08:02 GMT+0000 (Coordinated Universal Time)
cuid: clop6jvyd000109labdslfjal
slug: syncing-hashnode-to-wordpresscom
tags: developer-blogging

---

So these 2 days I have been trying to set up a synchronization tool between Hashnode and my Wordpress.com site. The WP site hosted my personal blog, which I usually use as a repository/journal. I have been blogging on the WP since high school.

Therefore I think I should port/save a copy of my Hashnode's post, into the Wordpress blog. I know there are a few strategies that could be taken, involving two main pathways (1) exporting from Hashnode, (2) importing to Wordpress :

Exporting From Hashnode

* API: Of course, one of the most robust and straightforward ways to access the content on my Hashnode blog is via the API. However, this means I have to write the code from scratch and set up an environment to run the script.
    
* RSS: Hashnode comes with built-in RSS features. I'm not sure whether RSS is still widely used, but I know it's a reliable tool.
    
* GitHub Integration: Hashnode includes a backup tool that saves posts in a GitHub repository as markdown (.md) files.
    

Importing to Wordpress

* Since I'm using the free version of WordPress.com, I have limited access to extended capabilities such as plugins, let alone writing my own script.
    
    XML-RPC: I had minimal exposure to this tool a few years back when I was experimenting with PHP. I'm not sure whether WordPress still supports this or not.
    
    Post-by-email: Perhaps the most basic, no-brainer, simple, and straightforward tool.
    

So, after a few attempts, I decided to use the combination of Github Backup and Post-by-email. I'm already used to git, and it's an opportunity to familiarize myself with Github actions. I can set up a Github Action that fires every time a post is pushed from Hashnode. The post will be saved as an MD file in the repo, and then the Github action will access the file, retrieve the Title and Content, and send an email with the Title and Content to the designated email address that will be automatically published on my Wordpress blog.

I will take my time updating the steps and tools that I used. In the meantime, I have to go for now, and I want to test whether this post is published in WordPress or not. See you later!