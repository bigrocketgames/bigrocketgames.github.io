---
layout: post
title:  "Creating a Sinatra MVC application."
date:   2017-01-01 01:35:32 +0000
---


When I first sat down to brainstorm for this project my mind immediately went to sports related themes, but I had a difficult time trying to tie the ideas into something simple.  Next I went back to the project page to read the directions and the ideas listed their.  Upon reading through and thinking for a bit, I finally came up with my idea.

Rather than having to get up and go look at all my movies on the shelfs, why not put them in a list that I could look at much quicker.  Then let others put their collections up as well for people to see and maybe find new movies to add to my collection as well.

I started by trying to figure out the setup of the database.  I knew I needed a users table and movies table, from there I sketched out what columns my tables needed and then did the migrations using rake.  Once I had the tables and classes created I began working with the controller.  I began with just a single controller but it became clear after a short bit that I was going to need more than just one controller.  I refactored my one controller into three separate controllers, then split my views into separate folders as well.

Next I began working on the views and getting the basic function of adding new users, logging in, adding movies, and so on.  The initial setup went smooth, but like usual getting all of the function with the database took a few extra minutes (ok, maybe an extra hour or so) to get just right.

My next to last step was to get the look right for the application.  I didn't want just a blank canvas, or something too basic.  I used bootstrap to make the application responsive and then went about some simple things such as a navbar across all the pages.

Once I had the look I wanted, I decided to go back and add some more features such as limiting what a user could see on another users collection page.  Not only did I not want users to be able to add, edit, or delete movies from collections that aren’t their own, but I decided I didn’t want those links to even be available to be seen.  This is where I had lots of fun because I could apply simple coding ideas to make the views more dynamic.

Overall I loved creating this project.  I loved the challenge of it and once again being able to apply everything I have learned over the last couple sections.  It was a ton of fun and I look forward to learning more and creating even more fantastic projects.

