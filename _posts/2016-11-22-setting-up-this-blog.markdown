---
published: true
title: Setting up this Blog
layout: post
tags: [tinypress, jekyll]
categories: [Howto]
comments: true
---
My first post is about how I set up this blog.

I knew that GitHub had a project called [GitHub Pages](https://pages.github.com/), which basically serves a static website for your GitHub project.
For this, GitHub uses a static site generator called [Jekyll](https://github.com/jekyll/jekyll).

I learned from my colleague [Sch3lp](https://sch3lp.github.io) that GitHub Pages can also be used for blogging and I liked the idea to have my blog tied to my github account.

My first attempt was to follow [these instructions](https://help.github.com/articles/using-jekyll-as-a-static-site-generator-with-github-pages/).
However, this was rather tedious, because it involves setting up Jekyll locally so you can build and preview your Blog before pushing your changes. It seems Jekyll and Windows don't get along and you need to do some [experimental setup](http://jekyllrb.com/docs/windows/#installation).

I decided I wanted an easier way to get started, asked google and bumped into [TinyPress](https://tinypress.co).
TinyPress does 2 things for you:

* First, it saves you from the hassle of creating and configuring your blog locally
* Next, it gives you an online blog editor with a live preview

TinyPress worked like a charm and saved me a lot of time!

Now that I am all set up, I could decide to break free from TinyPress and write my blogs locally.
I could do this by pulling the changes to my machine, see how TinyPress stores blog content, write new posts and preview them in an editor that supports markdown previewing, like [Visual Studio Code](https://code.visualstudio.com).

However, TinyPress offers some interesting features, like creating a post by sending an e-mail or delayed posting options.
They also offer an Android app, but I haven't tried it out just yet.
You can also add tags and categories to your post, but this doesn't seem to do anything.
I may have to read up on Jekyll and tags/categories in order for this to work...