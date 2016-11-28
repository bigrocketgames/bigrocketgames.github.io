---
layout: post
title:  "Creating My First Gem"
date:   2016-11-28 05:37:46 +0000
---


For the first Portfolio Project, I chose to create a gem that scrapes team sites on the Scout Network (www.scout.com).  I love sports, particularly football, and when sitting around with friends thinking of cool app ideas, we generally think of things relating to sports, so naturally my first instinct was to do something sports related.  Once I had the broad idea to use the scout network I needed to hone in on some specifics.   I decided to keep my focus on just NFL and NCAA FBS teams in order to keep my project from growing out of control.

My CLI Gem walks people through the process of choosing a team for which they want to see the most recent headlines.  Once a team is chosen, they will see the 20 most recent headlines for stories published on the team site.  After viewing the list of stories, they can choose a story to read the full text of if it is does not require the user to be a Subscriber to the site.

Before I got to really creating anything, I watched the video walkthrough of creating the Daily Deal CLI gem a couple of times to get a handle on the process of creation.  I knew what I wanted my gem to do, I just wasn't sure how to form it all, but this video gave me all of the information and resources I needed to get the job done.  I used Bundler to get the folder structure and main files setup then I went about using the same file/folder structure pattern as in the video as well.

Once I had the basic structure established I was ready to begin coding the project.  I started forming the CLI portion itself just using the NFL teams as I knew this would allow me to get the general layout I wanted without doing more than I needed to in case I didn't like something and wanted to change it.  Once I got into the project, I knew I wanted to have the scraper portion of the project to be its own class as it was going to be a bit more than what I first envisioned once I started playing around with the team sites and seeing that not all were exactly the same.  After working through some issues with scraping from not being super familiar with Nokogiri, I was able to get all of the information scraped, that I wanted.  Using pry during this process was super valuable as I was able to see things that I would miss otherwise.

Once the Scraper class was complete, I knew I was headed for the home stretch with my Story class and CLI.  I first set out to finish all of the methods I needed for the Story class to print out the story list and the full article text.  Once I was done with those methods, I moved on to the CLI and taking things for a full test drive with the NFL teams.  Upon my first full time through, I already had a list of five different improvements I wanted to make.  Things always seem great from the code side, until you test drive from the user side.  Thankfully, there were no major overhauls, it was just simple tweaks to clean things up, such as creating loops in the CLI for the case of an incorrect input that would exit someone out instead of asking for a valid input; or even the ability to go back to the previous menu, so as to avoid having to exit and then restart the app just to go back one menu.

Once I hashed all of these things out, I felt that great sense of accomplishment and knew I was ready to finish the project by adding the NCAA team information.  It took longer to hard code some of that information into the arrays, than it did to write most of my methods for the Story and CLI classes.  Once I was finished with it, I took it for a test drive, and immediately knew things were looking great.  Everything worked the way it was supposed to and I was overjoyed with creating something that just a few weeks ago I wouldn't have even known where to begin.

While it was not always easy to produce, it is one of my proudest creations since it shows how far I have come in just a short amount of time.
