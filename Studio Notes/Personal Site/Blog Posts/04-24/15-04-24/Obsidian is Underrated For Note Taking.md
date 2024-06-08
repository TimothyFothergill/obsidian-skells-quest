---
tags:
  - Personal-Blog
---
A strange topic but one I'm somewhat passionate about, after I've seen the benefits of it. I think solo development, whether it's on a passion project like a web app or a game, or as part of a day job as a developer, note taking is really vital. Today I'd like to walk through an app I use for note taking, how I get the most out of it for my solo projects and offer up a template I adore.
# Obsidian.md

[Obsidian](https://obsidian.md) is my note taking app of choice; it's available on Windows, OSX, Linux and now [Android](https://play.google.com/store/apps/details?id=md.obsidian&hl=en&gl=US) and [iOS](https://apps.apple.com/us/app/obsidian-connected-notes/id1557175442). It's free and the data stays in your hands, words that many software enthusiasts like to hear. On top of that, there are multiple ways for you to store your notes, so if security is a primary concern, this may be the app for you - And if you want ease of use, this can still be one to add to your software list!

![Obsidian Logo](https://obsidian.md/images/obsidian-logo-text-white-purple.svg)

### Obsidian Features

Here's a short list of features (and why they matter):
- Free 
	- There is a paid tier for commercial use for $50usd per user, per year. This gives you a commercial use license and priority support.
	- There are add ons as well, for syncing and publishing. Syncing enables syncing across devices; yearly cost of $28usd. Then there's publishing which publishes your notes to the web.
	- There's also an early access tier, which is a one time payment of $25usd or more (if you wish to donate to them)
- Plugins
	- There are hundreds of plugins, many of them are useful. Later in this article, we'll talk more about how I use them.
	- As far as I know, Obsidian Plugins are open source by default.
- Notes are stored as markdown files
	- Most people have used markdown, even if they don't realise it. Ever put \*\*'s around a word to make it bold? You've done some markdown!
- Your files live on your device
- The Graph View helps visualise your notes and what relates to what. Here's a few bug notes I took!

![Obsidians Graph View](https://i.ibb.co/FWsVx5Z/Graph-View.png)

## Taking notes as a solo developer

I won't lie, when I was getting started as a developer I didn't write notes down. I just drilled info into my head and hoped it would stick. I had been fortunate throughout my early career that things mostly stuck, but there have been times I would have helped myself by having notes. But it wasn't until I started trying different software out and settling on Obsidian did I feel comfortable with why I was writing notes.

My problem is when I write notes, I tend to put them in folders and keep them tucked away then never read them again. Obsidian lets me use hashtags to organise my notes, so I can go back to them by looking at the relevant hashtag. I also find that the way I write my notes was easily templated, but writing a templated style every time by scratch or by copy-pasting, was somewhat frustrating before I used the software.

### Obsidian plugins

![Obsidian Templater plugin](https://i.ibb.co/n8478fb/Obsidian-Templater-Plugin.png)

Plugins in obsidian completely transform how I take my notes. After installing the [Templater plugin](https://github.com/SilentVoid13/Templater), by just pressing `Alt + N` I can bring up my templates. I tend to have a format I use for all of them, but even better is when I choose one of them, it will automatically send the file to the relevant folders for me. This just required a little bit of code to make work:

```javascript
<% await tp.file.move("Tasks/" + tp.date.now("MM-YY") + "/" + tp.date.now("DD-MM-YY") + "/" + tp.file.title) %>
```

*Hope you find the new syntax highlighting and copy to clipboard functionality useful!*

With that code in place, if I hit `Alt + N` and select Task Templates, my next Task note will be placed in Tasks/MM-YY/DD-MM-YY, where DD is Day, MM is month and YY is year. This helps me keep everything tidy and chronologically ordered.

There's a lot more you can do with Templater, but hey, if none of this takes your fancy, you can always install the ObsidiDOOM plugin.

![ObsidiDOOM Plugin](https://i.ibb.co/L8Rbd78/Obsidi-DOOM.png)

What? DOOM runs on anything.

Go wild folks, happy tinkering! Much love and enjoy some note taking - 
Timlah