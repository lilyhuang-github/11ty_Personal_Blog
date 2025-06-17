---
title: Pr2
description: This is the blogs I've cread for the course OSD600, Open Source Development 600.
date: 2024-11-16
tags: ["osd600", "school", "software"]
---

So this Pr was onto the same repo. The previous pr I just ran into accidently since the spyder they had as an example in their documentation had an issue which is why I ran into it. This one I just went over each spyder to check for issues. This one was a bit more trickier cause it was a problem with the date parsing. One of the dates it was scraping had an apostrophe in it to indicate that the meetings been rescheduled but the parsing they were using couldn't handle so I just split it by the apostrophe, also the other issue was one of the dates didn't have a day in it, which is completely out of the standard formatting that the website uses/the chicago metropolitan pier and exposition authority normally uses, so I tried to fix it and the fix I ran into online was using dateutil parser which handles parsing dates that aren't in a strict format like datetime does.

I feel like I'm probably gonna make more prs for issues that I find/as I continue to find them
