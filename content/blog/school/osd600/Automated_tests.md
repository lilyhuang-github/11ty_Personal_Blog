---
title: Automated tests
description: This is my second blog that has been ported over from wordpress.
date: 2024-11-06
tags: ["osd600", "school", "software"]
---

So I used bun's built in testing tools and tried to use nock. I wanted to try to use mock to intercept the api call, cause the thing I did originally was try to make a fake openAI thing, like there's a bun module called mock which can fake/mock a module so I tried to mock the openAI module but It wasn't working and I also tried to make a class that inherits from the openAI class which almost worked but as I tried to do it it was like expecting more so I just assumed a different method would've been easier, which was making typescript ignore typing which is not great, so I tried to use nock so I can just use the actual openAI class and intercept it but it kept not intercepting it for some reason and got an error that the apikey wasn't correct.

I already change how it works a bit before in the rebasing but I also had to change the client so that it didn't automatically use the openAI class (since my plan was to try to override that class)

I ended up mocking it by having a different class that has the same dot operation things.

I didn't really have an aha moment, it was more of just a realization why people make the tests before they start coding cause I started dreading making the tests cause it would bring up issues in the original code that might not've come up if we started making the tests first.

I didn't really uncover any interesting bugs or edge cases, just that the code is somewhat frustrating to navigate. Like I built it in a way specifically for the commandline/yargs and not like a class or a standalone thing.

I think I should probably do tests first in the future, and also get a bigger picture on what the project should do since I think that'd give a better overview on what how things should've been designed.
