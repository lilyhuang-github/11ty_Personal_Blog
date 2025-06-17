---
title: Week 10 - Accessibility and dark mode
description: This is the blogs I've cread for the course OSD700, Open Source Development 700.
date: 2025-03-20
tags: ["osd700", "school", "software"]
---

With this week I did a bit more research on things.

My laptop that I normally do my work on is getting repaired so I’m working on an older laptop which me realize I should get a dock since I dislike a lot of things about this laptop which is why I wanted to try to do a more researchy sprint.

One of the things I realized was that accessibility is an issue that should be worked on from looking through the issues on Cockatrice.

The issue I was working on before my laptop broke was something that relates to accessibility: https://github.com/Cockatrice/Cockatrice/issues/5043. It’s about adding more keyboard controls since a lot of actions aren’t able to be done with a keyboard.

There’s this issue: https://github.com/Cockatrice/Cockatrice/issues/4278 which is about screen readers and how it can’t read a lot of elements in Cockatrice since most of the elements are qt image elements which don’t have a lot of support for screen readers. This kind of relates to a different issue that they had which was supporting different languages in the card text which since there wasn’t an easy way to swap things around.

This was when I realized Starchart could have a bit of focus on accessibility, most of the components being used are chakraui components which should be accessible so it shouldn’t be a major issue but it’s still worth it to test.

One of the things I tested was the contrast since I thought that It might be an issue due to things being red and one of the portions having black text on grey-ish background but it wasn’t an issue. I also used Window’s high contrast setting since I saw in an issue in cockatrice: https://github.com/Cockatrice/Cockatrice/issues/2388 about someone using a high contrast setting but then cockatrice not handling that really well, and the general idea of things shouldn’t mess with accessibility settings that the person has.
So I looked through with the high contrast mode and it didn’t seem like an issue.

I also tried to use a screen reader and navigate just using the keyboard. I couldn’t find an issue with it. There was an issue that I thought was an issue which was that the sentence would stop when it reaches a link, but I tested it on a bbc.com site which people say is accessible due to having the skip to content portion and it functioned the same so I think that one it functioning as expected. The other issue was trying to navigate the screen reader to read certain text which is a user problem on my end since I’m not sure if it’s user error (me not using a screen reader correctly) or if the site is not functioning correctly.

This lead me to trying to do automatic testing since I’m not entirely sure if my manual testing worked. I download an extension, axe devtools https://chromewebstore.google.com/detail/axe-devtools-web-accessib/lhdoppojpmngadmnindnejefpokejbdd which is meant to point out potential accessibility issue which I realized it should be integrateable into a CICD or a unit tester and it is and axe-core is the main thing people use like the vitest axe npm package https://www.npmjs.com/package/vitest-axe. Which is supposed to be like eslint but for accessibility.
Though, automatic testing doesn’t catch everything and you need to do manual testing.

Now this is kind of unrelated and more about accessibility but a lot of features are accessibility features but people don’t like to label them as accessibility features due to the stigma surrounding disability despite disability being something a lot of people experience or will experience in the future due to aging. Kinda crazy to be discriminatory to disabled people cause that’s like something people are eventually gonna face, even just temporarily, like someone might just need to use a wheelchair for a bit/not permanently due to some injury. But there’s a lot to talk about in this area and I’m just off topic. But stuff like dark mode I feel like is an accessibility feature since it’s something that helps people navigate on a website, just like how glasses are an accessibility tool but most people don’t view it as such.
