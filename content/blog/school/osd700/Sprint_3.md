---
title: Sprint 3
description: This is the blogs I've cread for the course OSD700, Open Source Development 700.
date: 2025-02-11
tags: ["osd700", "school", "software"]
---

I started a bit of work on hurl and got a pr(https://github.com/Orange-OpenSource/hurl/pull/3714).

The issue was that there was an argument that lets it capture the cookie for the hurl it does but it only let you do it to one hurl file. I.e you can’t do hurl file1.hurl file2.hurl –cookie-jar cookie.txt. And there wasn’t really a reason for why this isn’t allowed so it just needed to be adjusted so it was allowed.

The other pr i was working on was documenting the npm scripts for starchart(https://github.com/DevelopingSpace/starchart/pull/819)

The main thing was formatting which I don’t know if it’s good or not.

I started to try to work on cockatrice but I’ve run into a lot of problems with getting it to run locally properly. Cockatrice is a card game playing client but the main usage is for playing magic the gathering There’s like a micro service (or a similair term) called oracle. Oracle is what gets the card data for Cockatrice and I couldn’t get it running/it ran into some sort of issue. So I’m just working on getting that pull request landed and for any other issue in hurl as of tuesday. I’ll post an update if I get anything else done.
