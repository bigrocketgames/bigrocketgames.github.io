---
layout: post
title:  "Mixing Ruby with JS with HTML, oh my!"
date:   2017-05-07 18:32:09 +0000
---


So when starting to work on project 4 "Rails App with a jQuery Front End", I knew it was going to be a bit different and perhaps challenging to work with all of the languages.  I knew I could do it, but I wanted to make sure I kept it all clean and had a good follow through on the separation of concerns between the different languages.  While I knew I could it do it, I wasn't sure how difficult it would or wouldn't be.

Thankfully rails make this pretty easy to do with erb files and the automatic inclusion of js files through the asset pipeline.  Another fun trick I learned was through trial and error.  I was having an issue because I needed to be mixing ruby and js together, so I couldn't do it in a straight js file, and I didn't just want to make a huge html.erb file.  I knew that js.erb files could be produced and called up using the "respond_to" method in the controller, but that didn't seem like the right fit because I still needed all of the html.  

Next came the trial and error method to see if could create a partial in the js.erb format and get it to render.  So I created the file and tried to render it just like any other partial, hoping it would find the js.erb file and render it after not seeing a html.erb file of the partial name.  I was wrong and I got an error of course.  So next I set off to google and the rails guides on partials. I scavenged for a bit through the rails guides but didn't see anything directly relating to my idea.  I then went back to the handy rails error message.  This is the error I got "Missing partial recipes/script, application/script with {:locale=>[:en], :formats=>[:html], :variants=>[], :handlers=>[:raw, :erb, :html, :builder, :ruby, :coffee, :jbuilder]}.".  I almost immediately noticed the ":formats=>[:html]", it looked like it was specifically looking for a .html.erb file.  So I changed my render call from "render 'script'" to "render partial: 'script', formats: 'js'".  Voila!  The file loaded and I was able to simply render the js partial, so I could be using ruby with js in the same file without having a giant mess.  
