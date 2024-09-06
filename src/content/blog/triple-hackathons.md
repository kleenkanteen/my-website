---
title: My story of simultaneously doing 3, 1 week long online hackathons
author: Sabih Sarowar
pubDatetime: 2024-03-3T00:55:51Z
slug: triple-hackathons
featured: true
draft: false
tags:
  - coding
  - hackathons
description: "It was crazy."
---

Feb 16-23, 2024. One of the most intense weeks of my life. But it was worth it. It taught me a lot about making projects and my limits.

2 different sets of teammates for each. I found each of them and assembled the teams. I hatched the ideas for all of them.

Although for the 2nd one, my team brainstormed 3 ideas total, 2 were from me. After some deeper research my team decided to go with my 2nd idea.

I used clickup for docs + task assignment. It combined notion + trello beautifully. Discord for communication. Discord was crucial.

The hackathons were all due at the same day at 12pm, 1pm, and 6pm. I started coding at 9am that day. I had just a 30 minute lunch break. All ended at 6pm. Was spent by then. Coding for a deadline is stresful. It's not fun.

1. The first one was due 12pm. [GPT-4 Powered Hackathon](https://lablab.ai/event/gpt-4-powered-app-creation-hackathon). We tried turning a phone camera into a cashier system using gpt-4 vision. Take picture, get item and price added to cart automatically. \
   \
   From 9am-12pm I was trying to finish it. Got the inventory and cart page working. Only managed to finished 90% of it. Got stuck on the camera part. The camera only took a picture of the top 30% of the preview. I think this was a issue of the canvas element being smaller than the video element it covered. The camera input is is piped into the canvas I believe. But the canvas was samller than we thought it was. Yet to be resolved as of Mar 3.\
   \
   One of my other teammates was a talented 9th grader, a 15 year old Bulgarian teenager. He had high school but came home after and grinded this out daily until he went to bed. He was a passionate, hardworking young man with potential. He may not have been the most experienced but the effort and dedication was appreciated. He will go on to do great things.

2. The second one was due 1pm. [Developer Week 2024 Hackathon](https://developerweek-2024-hackathon.devpost.com/). Our idea used the European Space Agency's Sentinel-2 satellite images, publicly available, to show the soil moisure readings across a farmer's farm. You can input coordinate and get a colored image back of the soil moisture. My teammate tested the full flow and got it working. I just had to run it locally and present. But I had issues running it. I was missing one of my teammate's deployment environment variables so I was unable to demo it. I only had an hour to get it working. And I missed the deadline. Looking back, I wouldn't have enough time to demo it nicely. An hour isn't enough. I submitted it to a hackathon a month later and won best startup idea.

3. 3rd one was just bad teammates. Both from my uni, UTM. 1 was my year (5th), the other was 3 years below (2nd). Hackathon was the [Esri App Challenge](https://ecce.esri.ca/app-challenge/). The idea was that an user could input an address and then see a colored buffer on the map of how far they can walk in 5, 10, and 15 minutes. This is useful when choosing a new place to live. Helps see the walkability. The 2nd year teammate straight up gpt'd the code for the frontend map and location input then asked me for help when he got a bug. The autocomplete results were returning undefined in some of them. He was so confused on why it didn't work. Upon seeing his over commented, cliche code I could tell it was gpt'd. And asked him what it did. He said he had no idea.\
   \
   The autocomplete used this api: [photon](https://photon.komoot.io/). Look at how simple the queries are. And he had no idea how to hit it.\
   \
   Then I told him to rewrite it and use daisyUI components like how I wrote in the task.\
   \
   Third teammate basically botched the submission. If I had done his job we may have submitted in time. He used the mapbox api for the time distance buffers instead of esri's own api. This is an esri hackathon, we're supposed to use esri's technology at least in one place. So I to try using it in the frontend then. But esri had no react library. So I had to use react's dangerouslySetInnerHTML to render the esri map. But this took too long and I ran out of time. Couldn't finish it. I've learnt to identify lazy teammates early on. It's surprising how the 5th year didn't know the concept of testing your endpoint before handing it off. The guy didn't read the FastAPI docs I bet. Bad teammates aren't detail oriented. They know less because they searchfor less. It's better to have them do nothing than to mess up others.

In hindsight, had I put in more hours earlier in the week I could have finished. I could have always worked harder. But man I was close. They were solid ideas. I might come back to one of them. But there are too many interesting, higher impact ideas I want to make.