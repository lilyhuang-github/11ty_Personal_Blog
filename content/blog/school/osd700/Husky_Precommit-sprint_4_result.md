---
title: Husky Precommit - sprint 4 result
description: This is the blogs I've cread for the course OSD700, Open Source Development 700.
date: 2025-03-11
tags: ["osd700", "school", "software"]
---

One of the issues I was working on in Cockatrice was this one https://github.com/Cockatrice/Cockatrice/issues/2202. It’s meant to let the user choose between in-game time and real-life time for dating the actions.
Like:
[00:00:02] User1 Joined Game
[00:00:06] User1 Played Card
VS
[14:02:17] User1 Joined Game
[14:02:21] User1 Played Card
The top one measures from the start of the game counting up, the second one is the actual time for the player.
So I started to do that and ended up with this current PR https://github.com/Cockatrice/Cockatrice/pull/5709 that just starts it, and I’m going to have a commit later that implements the UI so players can select it.

Now, an issue I kept running into an issue where “i18n-default.json” kept getting changed whenever I try to commit. It kept changing it to removing the indentation so I assumed it was a linting issue and went on with trying to do the PR but it kept on getting included in my PR no matter what I did with git. Like I went to try to manually add each file I changed excluding i18n-default.json but it got included anyways and it just drove me crazy since I kept trying to do different things with git to not have it included. I did git rm and other things to try to stop it but I gave up and put the current PR I had on pause.

This leads to the other PR I had https://github.com/Cockatrice/Cockatrice/pull/5710. I realized that this is not reasonable at all, it shouldn’t edit the file in this way whenever I try to do a commit, and also undo me trying to undo the thing it was doing. But I figured it was like a husky precommit thing or a different tool that they were using that caused something to run. I also just knew it was husky since it was giving an error message mentioning husky. And essentially it was husky precommit that ran an npm script, the script runs a javascript file, the javascript file does something that I’m not entirely sure but it relates to i18n which is meant to help with translating projects, and it outputs the file with JSON.strinigfy but without any indentation arguments. So essentially whenever a commit happened it would run a command that would output into the file, but the problem was someone manually changed it to have indentation, and then whenever someone did a commit, it would automatically change it back to without indentation.
The only reason this didn’t become a bigger issue was probably because most people aren’t working on the web portion so they never came into this issue since they wouldn’t have husky run the precommit but since I did try to look at the web portion I kept running into the issue.

I also tried to do a bit of reviewing for starchart.
