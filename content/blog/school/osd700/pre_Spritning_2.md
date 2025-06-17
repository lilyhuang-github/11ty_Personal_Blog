---
title: pre Sprinting 2
description: This is the blogs I've cread for the course OSD700, Open Source Development 700.
date: 2025-02-01
tags: ["osd700", "school", "software"]
---

So the things I’ve done figuring stuff around bullmq, react 18 to 19, chakra v2 to v3, and node 18 to 20.

For the bullmq I created an issue for it in https://github.com/DevelopingSpace/starchart/issues/802. The reasoning is that from bullmq 4 to 5 they changed how the workers format their ID which affects how it goes into a queue which means it needs to change a bit and I’m gonna try to work on it next week.

From updating react 18 to 19. Apparently there was a big remake for it which is why a lot of things broke which I wasn’t entirely aware of, I just knew off of certain posts that people didn’t like that a lot of stuff broke between 18 to 19. But it also broke chakra v2 which meant it needed to be updated to chakra v3 but chakra v3 breaks a lot of things as well since they apparently also re wrote their things which also from other posts I’ve seen made people not like it and want to switch to something like shadcn. I tried to do it in this PR https://github.com/DevelopingSpace/starchart/pull/790 but now it’s probably not gonna happen since it’d be a large rewrite and also react 18 is probably gonna have a lot of support.

I’m now trying to get the node version to a more LTS version since chakra v3 wanted node 20 but also because that was my original goal.

I didn’t entirely know how you would update the node version so I just went off of what other people said which was to update the packages first so I did that but also I didn’t know if I Was missing something. Like I just changed some of the text mentions of node 18 to 20, and the docker and github action files to node 20 but that felt like not a lot. So I felt like I was missing something obvious that needed to be change but it’s fine.
