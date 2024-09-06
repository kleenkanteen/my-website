---
title: How it's like being a lead engineer at a pre-MVP startup
author: Sabih Sarowar
pubDatetime: 2024-09-06T00:42:51Z
modDatetime: 2024-09-06T00:42:51Z
slug: lead-engineer
featured: true
draft: false
tags:
  - coding
  - startup
description: "It's fun and interesting."
---

# What is Keepsake

[Keepsake](hellokeepsake.com) is a website that reduces manual work for estate planning lawyers (who you go to write a will and stuff). All they do in their jobs essentially is to collect info from clients, sometimes verbally in a meeting, use that to fill out forms, and then draft up the legal docs. Quite repetitive. Perfect for a tool to help them save time. 

Keepsake is a pre-MVP startup with the planned launch date at sep 30. There are 5-10 lawyers on the waitlist who will pay upon MVP launch. The word startup sounds a bit weird, as if you got VC funding, which we got none of. Think of it more as an early stage SaaS.

There is 1 major competitor, DecisionVault. The founder made it after seeing his wife, an estate attorney, tediously filling out PDF/paper forms. So he made a site to collect this info in a online form. The idea for Keepsake is to be a step above this in automation. And many lawyers don't use any online form site, they just send a plain PDF to clients.

# History of Keepsake

Keepsake was founded in Jan 2023 by 2 USC students (uni of south cali, expensive private uni). They are Justin and Isabella, if you go on linkedin and search the company, you can see their profiles. They majored in business and graduated in May 2023-ish. They turned down job offers after graduation to pursue Keepsake full time. They first got the idea when one of them as a child had their grandma pass away and collecting her info and life memories was difficult. The idea was originally for people to collect their personal info to pass on when they. But the couldn't validate the idea and after pivoting a couple times by going to senior homes, holding focus groups, reaching out to home organizers and a few other professions, estate lawyers resonated most with the idea. In one call, a lawyer actually had an epiphany and suggested the idea to help lawyers automate their form collection process. So the 2 founders pivoted to the estate lawyer idea and got to work in Jan 2024. 

Justin and Isabella put a ton of time into Keepsake, and you could realize by seeing how many lawyers Justin called and how expansive and detailed Isabella's Figma is. Finding people who are hardworking outside of school is rare in my experience. Most CS students don't have side projects or consume programming content on their own. It's what you pursue on your free time that defines you.

Justin is sales, he did the cold calling and emailing to get leads. He gave 50 30 min demos. He basically said he gets 1 demo for every 2 hours of cold calling. That's at least 100 hours of cold calling just to get those demos. 

Isabella does design and made this huge figma for the project, she's pretty good at it. Before me they had this one lead engineer who was part time and a USC student, Abby. She made most of the website so far but left in Mar 2024, had too much going on.

Their work speaks for itself.

After that, they brought on another dev as the lead engineer after Abby left. He had about 7 years of exp as a developer but wasn't hardworking. Looking at the commit history, he didn't do that much which caused them to constantly miss deadlines. Didn't exhibit the qualities of a lead engineer either, there was a PR backlog of 20 tickets from 2 months when I joined. Merge conflicts were abound. This lack of dev speed made it so that lawyers who were promised the product at x date would have that date repeatedly pushed back. This probably affected goodwill. The lead engineer got demotivated himself due to pressure of deadlines from the 2 founders and eventually left on his own accord. Wasn't a nasty exit as least, both sides wanted to part.

# How I entered

Justin found me on the YC cofounder matching site around June 15, 2024. I was 2 months out of my CS degree and was still job searching so I had time. I was on that site to see who would be interested to share ideas, have interesting convos, and possibly find someone to work with. Won't lie, the majority there are not of quality and will ghost you. Ironic because it attracts a certain crowd, more ambitious than usual, and most of them will ghost you or not communicate properly. Justin was good though and sent me a detailed document about Keepsake before we had our intro call. Long story short, I got on a trial and 2 weeks later he offered me the lead engineer/CTO position. I liked that it was validated and in a niche market so accepted it. I thought the chances of making significant revenue was good and wanted to make my first internet dollar and more.

# My sweeping changes

As of Sep 5, the team is the 2 cofounders + me + 4 other devs. 3 of the devs I knew from before and brought on. The 4th one was a USC intern.

In more detail about the team: In late Aug, I brought on 2 new grads I worked with before. Both are doing great work so far (as of 2 weeks), especially on this large codebase of 50k lines. The third guy I brought on is an incoming first year CS student in Illinois. Worked with him on a clinic robocaller project I had abandoned before giving to him as he was looking for a project to work on. He did great on it and is currently doing great. 

The last guy is a USC new grad whose job starts in Jan. Until then he will be with us. Keepsake used to rely on unpaid interns before I started but soon after I joined, I chose to only have paid devs who committed at least 20h/week. Because paid devs are motivated devs. They either get deferred pay (when we make revenue) or profit sharing + equity. We make $0 right now as we are pre-revenue. I get 15% equity over 2 years and 20% profit sharing moving forward. 

I instituted this 20h/week and paid devs only rule in the last week of Aug and that's when work started to really pick up. PR's would get merged almost daily. I also increased my time commitment and do 30-40h/week.

# The pains

The pains of my role is that that some of the tickets are too large and should be broken up. Once this caused wasted work as one dev did duplicate work of another one. Or the ticket is poorly written so it needs clarification. The tickets were written like 7 months back in Jan so it's understandable to an extent. I or a dev have to ask Justin/Isabella for clarification. We'll all get better at it though, it's an art.

# The fun

The interesting part is that I get to work in a software team that is similar to the real world. It's fun. I was in a rut when things in Keepsake were slow in July. The whole month actually. My sleep schedule was wack. I couldn't find an idea that excited me, even though I had 100 ideas written down, some that were pretty good. I wanted to work on something more serious with a team. Like how my 1 year fullstack internship was. It's fun working with others. In late Aug, after guaranteeing a committed team with the 4 other devs, speed picked up. Things are being made, technical problems are being solved. It's getting close to a real job.

I did have experience leading devs as I did 6 online hackathons in the 6 months preceding that. Each were 20-30 hours of total effort, on average from 3-7 days. Each was with 2 other devs that I had sought out and invited. I learnt how to identify talent (look at their github), plan a project, write tickets, break them down to manageable size, and communicate well. I learnt how to ship something from scratch as a team, as ragtag as it was. Keepsake is a level above that. It's like a serious hackathon but the idea has market validation and you're not just working on it for a couple days.

# How I am doing

You might be wondering, how am I doing as a lead engineer/tech lead? A dev today told me I am doing well and I was flattered. I think I'm doing an average job. I'm spending so much time communicating instead of coding. I have a high level view of the tickets so I've been able to prevent duplicate work or question something that is low value so the other 2 founders agree to leave it out of the MVP.

The past 2 weeks I have not been able to write code. I did do a good bit of aws and gcp setup for devops stuff though. Most of my time is communicating, such as asking for clarification on tickets on linear from Justin and Isabella, or suggesting we leave x out of the MVP since it wouldn't bring much value. Or I respond to dev questions about their tickets and jumping in a call to help out. I do feel productive. But not as much as when I finish a feature, such as when yesterday I got ci/cd set up on the staging branch to autodeploy to gcp cloud run for every commit. That felt good seeing my (config) code come work and do something impactful.

Hopefully I can manage well enough so at least half of my time can be spent coding. I hope Keepsake makes a lot of money and I can learn what it takes to take a SaaS from $0 monthly revenue to $100k as the lead engineer. There's a long road ahead for me and for Keepsake and I'm looking forward to it.