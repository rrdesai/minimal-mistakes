---
layout: default
title: "Optimizing with MTA data"
date: 2016-09-27
categories:
  - Explorations
description:
image: 
image-sm:
---

##  Week 1 @ Metis NYC

The first week at [Metis](link) was an absolute blur. Even with a background in Python & data analysis, between brushing some rust, picking up tips and tricks, and exploring new packages, there was a lot to take in. On top of all that we dove into the MTA turnstile dataset on day one as part of our first project: optimizing a hypothetical street team based primarily on this MTA turnstile data.

#### Step One: Data Acquisition and Cleaning

The first step in the process was getting the data down from the MTA site. The entry and exit counts in the dataset are absolute for each MTA turnstile and thus need to be adjusted to get daily counts, summed for each station, and then scrubbed for illogical values. After getting the data in the correct format, I removed values over 1250 entries or exits per hour for an individual turnstile as well as negative values. I then summed the turnstiles so the data had one row per station per day.


#### The Project
Since this was our first project, we actually worked in groups for the majority of the process. As you would expect since this was the first week of the program, there was a lot of variance in individual comfort levels. We got lucky that everyone in our group had some experience with analytics and could contribute in one way or another. Since RJ also had pandas experience, he handled a lot of the data management while I took point on the graphing.

Before we got to visualization though, we had to make a few cuts to get the framework of our strategy. Since we were optimizing a street team trying to collect email addresses for a local nonprofit total traffic per station was the obvious top level filter. Although this did cut out a lot of stations even taking the top ten percent of stations by traffic left us with nearly 50 options! (We're not in Boston anymore, huh?)

At this point we had to bring in some other datasets so we settled on income data from the census as well as looking at where the tech hotspots in NYC are located. I was also able to draw on my experience actually optimizing canvassing teams in Boston, namely to say that people are more likely to stop and talk on nights & weekends and that more traffic is not always better!

We ended up looking at how traffic varied with season, day of week, and time of day and made some pretty interesting heatmaps (linked below) to illustrate the flow in top stations. Our final recommendations were split by weekday and weekend as well as morning, afternoon, and evenings. If we had to choose we would focus on Manhattan for all blocks, hitting commuter stations (Penn Station, Grand Central) during the morning and evening rush on weekdays while venturing to places like Union Square in the afternoons to get the lunch and tech crowd. On weekends we would recommend going to stations based on our income and tech neighborhood data. For residential stations a prime candidate is 86th street while Chambers St and W 14th Street are great options to catch the tech/weekend crowd!
