---
layout: post
title:  "Jekyll is my friend... maybe"
date:   2016-02-25
categories: TIL
tags: [jekyll, TIL]
---

So ive decided to try and document my daily learning using markdown, jekyll, and github pages. I say daily but I am mostly refering to week days, however if i get something over the weekend ill call it a bonus... This will be a challenge for me just to put my thoughts on paper (ok not really paper...)
anyways i guess ill get started

Setting up this page alone included quite a bit of learning just getting jekyll setup and looking decent. It took a bit of time but i think im starting to wrap my head around how it works and should be set up. The main thing i wanted to do on it to start with was to have it display the whole post instead of only the title and date like it came with. To do that i first had to figure out where that file was even located. i finally realized its in the root directory in a file called index.html (seems obvious now...)

By default it only shows the post title ( \{\{post.title\}\} ) and links to the post ( \{\{ post.url \}\} ), but i wanted to have all posts there inline (also added pagination). 

maybe monday i can learn how to post the snippet of code to detail this...

... no luck on that snippet but i made a screenshot.


![alt text](/img/jekyll_post_loop.png "jekyll_post_loop")

obviously the first { % starts the loop and as long as there are more posts it will spit them out. and the endfor bit ends the loop.

