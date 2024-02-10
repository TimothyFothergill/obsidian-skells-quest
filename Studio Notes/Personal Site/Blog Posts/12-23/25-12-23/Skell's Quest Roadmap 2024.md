---
tags:
  - Personal-Blog
---
Let's start the new year off by discussing my largest ongoing project and what the next year looks like for it, as well as what happened in 2023. There's also a quick bit of git shenanigans in the middle, so if you're interested in knowing certain metrics for your own projects, this might be a neat one-liner for you (If you're using git to manage your projects).

![Meet The First Boss, Blobob, the Devourer. Imaginative, I know.](https://i.ibb.co/N236FTq/Blobob-The-Devourer.png)
# 2023 Recap
In 2023, I managed to deliver 4 versions of Skell's Quest, the latest of which can be played [here](https://play.unity.com/mg/other/skell-s-quest-v0-0-4-prototype). I was hoping to have 0.0.5 out by now, but as mentioned in a recent article, I've had some real-life changes which needed to be dealt with first. Now I'm done, here's a small look at what I've done on Skell's Quest and the future.

In 2023, I made a lot of changes to files, lots of meta files, lots of code, lots of shaders - You name it. 

```
 267 files changed, 126437 insertions(+), 21913 deletions(-)
 20 files changed, 28295 insertions(+), 3117 deletions(-)
 1822 files changed, 234565 insertions(+), 284853 deletions(-)
 33 files changed, 9725 insertions(+), 3220 deletions(-)
 1955 files changed, 307142 insertions(+), 60086 deletions(-)
 161 files changed, 58897 insertions(+), 4021 deletions(-)
 738 files changed, 64255 insertions(+), 6109 deletions(-)
 669 files changed, 45505 insertions(+), 112 deletions(-)
 137 files changed, 38596 insertions(+), 30108 deletions(-)
 ```
 **Totalling: 5802 files changed, 913417 insertions, 413539 deletions** (Assuming I mathsed good)

So these are some of the merges to my main branch and as you can see, that's a lot of files, insertions and deletions. I was able to get this information with the command `git log --oneline --shortstat`. However, I found you can also specify file extension types by adding a further `-- '*.{extension}'`. The insertions and deletions above are for everything. This includes generated lines of JSON and YAML data, of which a single file can be hundreds or even thousands of lines.

So the above isn't very instructive, albeit I like seeing big numbers. The below however is all C# code changes for the game:

```
 27 files changed, 742 insertions(+), 129 deletions(-)
 6 files changed, 140 insertions(+), 242 deletions(-)
 338 files changed, 36308 insertions(+), 35224 deletions(-)
 9 files changed, 248 insertions(+), 2 deletions(-)
 255 files changed, 27371 insertions(+), 245 deletions(-)
 27 files changed, 410 insertions(+), 154 deletions(-)
 49 files changed, 1753 insertions(+), 171 deletions(-)
 43 files changed, 2265 insertions(+), 5 deletions(-)
 41 files changed, 1902 insertions(+), 862 deletions(-)
``` 
 **Totalling: 795 files changed, 71139 insertions, 37034 deletions** (Assuming I mathsed good)

## Where's The Next Update?
So I'm thinking the next update will be the last major one for a while. Instead, I want to begin work on assets which will take me a long time, as I'm not the best at making assets. Some of the things I've made previously include this fetching little array of tailoring materials:

![Tailoring materials in the game](https://i.ibb.co/ZW9YW5T/Tailoring-Station.png)

And this pretty naff little anvil:

![This anvil could do with a better model](https://i.ibb.co/r353sPm/Smithing-Station.png)

I've also made most of the icons for the skills in the game, such as these two:

![Botany]( https://i.ibb.co/F0g7bKm/Botany.png)

![Wildcrafting Icon](https://i.ibb.co/jM7FJct/Wildcraft.png)

This doesn't fully answer the question, but in short, the next update features a playable dungeon with lots of new features. I'm excited to get this update out, but it's a lot bigger than I anticipated. As such, I'm going to put all my efforts into making this update a really big one, before just working on assets for the rest of the year (with a few code changes every now and then to keep my interest level up!)

I may also work on the story, make all of the items and figure out scaling... And some internal tooling. My goal for this year as well is to write plenty of blog posts, at least once per week. Expect to see more.

That's about it, but I'm excited to get on with Skell's Quest this year. I've got so much to do, but every challenge is a worthwhile one. Once I have more information about the upcoming update, I'll share more.

Until next time, much love and keep on tinkering - 
Timlah