---
title: Updating stuff.
description: This is the blogs I've cread for the course OSD600, Open Source Development 600.
date: 2024-09-13
tags: ["osd600", "school", "software"]
---

o the way I went with doing my code reviews was asynchronously cause scheduling. You don't really have to deal with a specific time, you just do it before a certain and it kinda works.

It was kinda hard reviewing someone else's code cause stuff just works. or, my main issue was how user friendly instructions have to be (both for someone else's repo and my own) cause github is a code sharing platform, so the intention is to share with other developers so there's a bit of an assumption of competency in understanding some of the stuff, but some people use it as an actual download page, so they're expecting people/users, i.e potentially non technical people, to actually download their stuff off of github. Like i've seen stuff on twitter of people complaining about that, and like not understanding how you're supposed to download stuff off of github and running stuff after downloading it, so it's kinda just confusing how specific stuff like that needs to be. You'know like should stuff with explaining how to add an ssh key and all that be apart of the guide and how to install npm or python and then how to use a cli to do stuff like npm run install and what not.

It was ok having someone test and review my code. My main thing was sort of a realization. Cause I add a lot of comments that are more specifically for myself. Like to take notes on how stuff works and what method would be better, like stuff that might not directly relate to the code and explaining to another person.

There's some other issues. Like the readme not being clear/correct and the help command not entirely being correct I was kind of all over the place with things. Like I was kind of trying to plan ahead. Cause my main problem was with what I should make the cli app do but it was kind of hard to figure that out but I can't just sit around and try to figure that out so I went ahead and started working but then i changed what it was supposed to do and subsequently what it was named and that made the readme and help command incorrect and I was also gonna implement like a link type thing where you just type the cli app name so you don't have to directly reference the file (i.e not having to type bun index.ts)

This was one of the issues I filled: https://github.com/arilloid/addcom/issues/1 , It's like just that they should change the client from groq to openai so that they could do the call to any api endpoint and not just for groq. Which is also mentioned in a different issue: https://github.com/arilloid/addcom/issues/3. My other issue was it should do a version flag: https://github.com/arilloid/addcom/issues/2. My main problem was not really knowing what issues to give. Cause there isn't really any issues I can see in the code besides missing some features but just saying that it's missing some features isn't really helpful cause they're still being implemented.

With my issues there was this: https://github.com/lilyhuang-github/rat-assistant/issues/9 which was the help flag isn't accurate since you have to run the file with bun and I had to fix that with a shebang and a linkage so they could just type the name to run it so it's accurate. And typos: https://github.com/lilyhuang-github/rat-assistant/issues/10 and formatting issues which I've fixed: https://github.com/lilyhuang-github/rat-assistant/issues/8

I haven't fixed all the issues mentioned but I'm going through them.

What I've learned is that it's a lot of work to make something usable for someone else. Like I still have more stuff to add/remove to make it more useable/understandable to a dev and then it'd be a lot more probably for an end user.
