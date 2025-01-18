---
title: How it's like being the tech lead at a pre-MVP startup
author: Sabih Sarowar
pubDatetime: 2024-09-06T00:42:51Z
modDatetime: 2024-09-06T00:42:51Z
slug: tech-lead
featured: true
draft: false
tags:
  - coding
  - startup
description: "It's fun and interesting."
---

# Intro

[Keepsake](hellokeepsake.com) is a webapp specifally for inheritance lawyers (they makea trust or will). All they do in their jobs essentially: 
1. Collect their clients assets, and decisions on how to to distribute them.
2. Store that info somewhere
3. Draft up the 70 page will/trust document, and have them both sign it. 

This is overlyversimplified, but there's different ways of arriving at the final legal document. You can do this through a clunky, paper process. Or with a streamlined, digitized process, that passes data to wherever you need it. Our goal is maximize their efficiency when doing all this. I've had one lawyer tell me that he wants to be more efficient. Some of them know that they can do better, especially as their client volumn increases.

Back to Keepsake: we are a pre-MVP startup. There are 28ish lawyers on the waitlist, who each got a 30min demo of the figma mockup, back in Mar-Apr 2024 by Justin, the sales cofounder. Half of them said they'd be willing to sign up upon launch, and the other half said they're interested, but are waiting for launch before they decide.

The word startup sounds a bit weird, as if you got funding from investors, which we got none of. We are fully bootstrapped.Think of it more as an early stage SaaS.

There are 2 major competitors: 
1. DecisionVault: The founder made it in 2020, after seeing his wife, an inheritance lawyer, tediously having to re-type 34 different people's information, from paper to computer. So he made a site to collect all this info in an online form, and automatically pass contact info around. Many lawyers don't use any online form solution, they just send a plain PDF to clients, which clunky and hard to organize. You can't work fast when client data is stored in a PDF. DecisionVault is stable and great, but the founder is happy with his growth, and doesn't want to vertically expand. He is bootstrapped as well and has kids. The guy picked up coding just to make DecisionVault. Competent, strong entrepreneur.
2. Legacy Architect: The founder is a estae inheritance lawyer herself, with 13 years of experience. Great vision, but I think she outsourced development. Lawyers who used her site have said it was buggy. Does work for the most part, but is lacking on the execution side.

Basically, the space is contested. As one lawyer who uses Legacy Architect told us, no one has cracked the whole estate planning workflow from start to finish. There is opportunity to build the tools of the future, for the [200k](https://www.ibisworld.com/industry-statistics/number-of-businesses/estate-lawyers-attorneys-united-states/#:~:text=There%20are%20202%2C423%20Estate%20Lawyers,increase%20of%200.4%25%20from%202023.) inheritance lawyers out there.

# My entrance

When I joined, I inherited a codebase with 50k lines of code, and a shoddily configured deployment, using AWS ECS (elastic container service). Basically 0 documentation on both. The secrets for the staging and production deployments were both stored in separate .env files, inside a s3 bucket, instead of being pulled from secrets manager. Irrationally from whoever set that up. Apparently they were a early career devops specialist too, according to their Linkedin.

Note: The meat of this article was written on Sep 6, but I write the next 3 paragraphs on Dec 24. I had cleaned up the deployment mess by switching over to GCP cloud run, and brought in 3 of my talented dev friends part-time, at 15h/week. We made incredible progress from Sep-Dec, and launched the beta in early Nov.  We are currently in beta with 2 lawyers, one of who has sent his forms to 2 real clients last week. They will take about 3 weeks to fill it out. We are hoping to launch the MVP, with improvements from beta, in late jan. 

It's been a ride and over the past 2 months since Nov 1. I've met with 11 different lawyers, 1 paralegal, and 2 assistants, over 21 meetings. Some lawyers are repeat ones, like those in our beta. I met our closest beta lawyer, the one 4 different times, over 6 hours total, before he sent it to 2 real clients on Dec 15. Didn't have to be that long as we got chatty, but that shows how much work is required to convince your first beta user. 

Nonetheless, over the 11 demos, I got a lot of feedback about our UI and features. I see where the opportunity is. And the team has changed drastically since Sep 6. The original founders, both 1.5y out of school, had to get jobs. I had to lead this solo. And I'm still excited to get the MVP launch going!

Back to Sep 6 now.

# History of Keepsake

Keepsake was founded in Jan 2023 by 2 USC students (uni of south cali, expensive private uni). They are Justin and Isabella, and if you go on linkedin and search the company, you can see their profiles. They majored in business and graduated in Apr 2023. They turned down job offers after graduation, just to pursue Keepsake full-time. They first got the idea when one of them as a child, had their grandma pass away. Collecting her info and life memories was a pain. 

The idea was originally for people to store and pass on their memories. But they couldn't validate the idea. They did a discovery phase by going to senior homes, holding focus groups, and reaching out to home organizers and a few other professions. But it was hard inheritance lawyers that resonated most with the idea. In one meeting, a lawyer had an epiphany, and suggested the idea to help lawyers streamline their workflow. The 2 founders then pivoted to target just lawyers, and got to work in Jan 2024. 

Justin and Isabella put a ton of time into Keepsake, and you could see this by seeing how many lawyers they reached out to. Justin did 100-300h of cold calling, Isabell made a huge, expansive Figma mockup. Finding people who are hardworking outside of school, is very rare in my experience. For example, most CS students don't have side projects or even have time to consume programming content in their free time. It's what you pursue on your free time that defines you.

Justin is sales, he did the cold calling and emailing to get leads. He gave about 30ish, 30 min demos. He said he gets 1 demo for every 3-6 hours of cold calling. That's at least 100 hours of cold calling just to get those demos. 

Isabella does design and made this huge figma for the project, she's pretty good at that. Before me, they had this one lead dev, who was part-time and a USC student, Abby. She made most of the site, but left in Mar 2024. She had too much going on, being in school clubs and all, and Keepsake wasn't popping off.

After that, they brought on another dev as the technical cofounder after Abby left. He had about 7 years of exp as a dev, but wasn't hardworking. Looking at the commit history, he didn't do that much, anything even, which caused them to constantly miss deadlines. He didn't exhibit the qualities of a lead engineer either. When I joined, there was a PR backlog of 20 tickets, of a few different part-time devs who were on on the team. They ranged from 1 week to 2 months old. Merge conflicts were abound. 

His lack of dev speed made it so that lawyers who were promised the product in April, would have that date repeatedly pushed back, the night before even. And their schedule is usually booked a week in advance. This harmed trust with lawyers. He got demotivated himself a well, due to the pressure of deadlines from the 2 other founders and eventually left on his own accord. He left 2 weeks into when I joined. It wasn't a nasty exit as least, both sides wanted to part. He got demotivated, and the 2 founders were not happy with his results.

# How I entered

Justin found me on the YC cofounder matching site on June 15, 2024. I was 2 months out of my CS degree and was still job searching, so I had time. I was on that site to see who would be interested to share ideas, have interesting convos, and possibly find someone to work with. Won't lie, the majority there are low quality and will ghost you. It's ironic because I thought it would attract a certain crowd, ambitious nad hardworking, but most will ghost you and not even chat casually. 

Justin was different though, he found me and messaged me first. He asked for a call to chat, and I asked for any details about the idea in preparation. He sent me a 20 page long document about what Keepsake is about, and the market research. I had 15 people before him reach out, and all they gave was a few sentences of details max. No one gave a document. 

Long story short, I joined on a trial, and 2 weeks later when the previous technical cofounder left, I got offered to lead development. I accepted, becauseI liked that he had talked to 30-50 lawyers, and got some traction. It was validated and in a niche market. I thought the chances of making significant revenue was decent, and wanted to make my first internet dollar.

# My sweeping changes

As of Sep 5, the team is the 2 cofounders + me + 4 other devs. 3 of the devs are friends of mines that I brought on. The 4th one is a USC intern.

More details about the team: In late Aug, I brought on 2 new grads I worked with before. Both are doing great work so far (as of 2 weeks), especially on this large codebase of 50k lines. The third guy I brought on is an incoming first year CS student in Illinois. Worked with him on a clinic robocaller project I had abandoned before giving it to him. He did great work on it, and is currently doing great. 

The last guy is a USC new grad whose job starts in Jan. Until then he will be with us. Keepsake used to rely on unpaid interns before I started but soon after I joined, I chose to only have paid devs who committed at least 20h/week. Because paid devs are motivated devs. They either get deferred pay (when we make revenue) or profit sharing + equity. We make $0 right now as we are pre-revenue. And I get 15% equity over 2 years, and 20% profit sharing moving forward. 

I instituted this 20h/week and paid devs only rule in the last week of Aug. That's when work started to really pick up. PR's would get merged almost daily. I also increased my time commitment and do 30-40h/week.

# The pains

The pains of my role is that that some of the tickets are too large and should be broken up. Once this caused wasted work, as one dev did the duplicate work that another already did. Or a ticket would be poorly written and needs clarification. Many tickets were also written like 7 months back in Jan. I or a dev have to ask Justin/Isabella for clarification. We'll all get better at it though, it's an art.

# The fun

The interesting part is that I get to work in a software team that is similar to the real world. It's fun. I was in a rut when things in Keepsake were slow in July, around when I joined. The whole month actually, my sleep schedule was wack. I was sleeping at 5am. I couldn't find an idea that excited me, even though I had 100 ideas written down. I wanted to work on something more serious with a team, that had traction, like how my 1 year fullstack internship was. It's fun working with others. And then with Keepsake in late Aug, after guaranteeing a committed team with the 4 other devs, speed picked up. Work was being done, technical problems were being solved. It was getting close to a real job.

I did have experience leading devs before. I did 6 online hackathons in the 6 months preceding that. Each were 20-30 hours of total effort, on average from 3-7 days. Each were with 2 other devs, that I had sought out and invited. I learnt how to identify talent (look at their github), plan a project, write tickets, break them down to manageable size, and communicate well. I learnt how to ship something from 0-1 in a few days. Keepsake is a big leap above that, but my past experince was a stepping stone. Now it's like a serious hackathon, but the idea has some validation, and you're working on it for months.

# How I am doing

You might be wondering, how am I doing as the tech lead? A dev today told me I am doing well, and I was flattered. I think I'm doing an average job. I'm spending so much time communicating instead of coding. I'm being available and helping out teammates. I have a high level view of the tickets, so I've been able to prevent duplicate work form being done, or communicate if I think something is low value. But I can't write much code.

The past 2 weeks, I have not been able to write any code. I did do a good bit of aws and gcp setup for devops stuff. But most of my time is communicating, such as asking for clarification on tickets written by Justin/Isabella, or suggesting we leave x out of the MVP. Or I respond to dev questions about their tickets, or jumping in a call to help them out on it. I do feel productive. But not as much as when I finish a feature, such as yesterday, when I got ci/cd set up on the staging branch to autodeploy to gcp cloud run for every commit. That felt good seeing my config code come to life and do something meaningful. Helping others is meaningful as well though.

Hopefully I can manage well enough so at least half of my time can be spent coding. I hope Keepsake makes a lot of money, and I can learn what it takes to take a SaaS from $0 to $100k monthly revenue. There's a long road ahead for me and for Keepsake and I'm looking forward to it!