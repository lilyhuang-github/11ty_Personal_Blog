---
title: Static analsis
description: This is the blogs I've cread for the course OSD600, Open Source Development 600.
date: 2024-10-30
tags: ["osd600", "school", "software"]
---

So the automatic source code formatter I used was Prettier and linter was Eslint.

The project build scripts I had were just bun run scripts that ran prettier and eslint. The only issue was sometime I thought about before where I wanted to make it compatable with other things and not just bun, so it'd be able to use npm/pnpm/bun etc, but I couldn't find an easy way to do that. Cause, I found that the format of the run script is basically the same, its bun run script, npm run script, and pnpm run script, so it should all pretty much have the same build scrip. This is a link to eslint: https://eslint.org/ and prettier: https://prettier.io/. I just chose them since they're the ones I've used before.

I also used the prettier and Eslint extension with vscode and moved a lot of the documentation over.

Also explained how you can use the run script and also added a githook. I looked into how you could add a githook and the simplest/most common that I saw was using husky.

They didn't find a lot of issues. With eslint it just found some simple to change stuff like changing stuff from let to const since it didn't change.

I got the tools to run from the command line by adding them to the package.json so you can use bun to run the script that'll run the package.

I intergrated the tools to my ide with the prettier and eslint extesnion and edited the vscode json settings so that it automatically does the prettier formatting when it saves and the eslinting show up in the problems in vscode.

I also added the githook that does the linting and formatting pre-commit, though, I feel like it should do it before or somewhere, cause the issue I feel, is that I commit, and then it does the githook and changes things so the current files are different from the commit that was made, so then you can commit again, so it probably needs to commit at a different time.

But I learned a bit, I was mainly using git through the cli and trying to not rely on vscode, and learning about the githooks.
