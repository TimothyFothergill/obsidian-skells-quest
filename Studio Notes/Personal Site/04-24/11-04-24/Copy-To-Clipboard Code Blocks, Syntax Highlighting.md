---
tags:
  - Personal-Blog
  - Markdown
---
*Start time:* 22:52

**Story:** 
As a reader of the blog,
I want to be able to copy large code blocks,
So I can paste them in to try myself

As a reader of the blog,
I want to see a code block have the correct syntax highlighting,
So it is easier to decipher the code

**Acceptance Criteria (as appropriate):**
- Code blocks with triple backticks can be copied to a clipboard with the click of a button.
- Code blocks with triple backticks have syntax highlighting.

**Comments:** 
As a bonus to this ticket, I'd like to make the syntax highlighting automatic, rather than the author (me) needing to specify the language.

I can use node for the syntax highlighting with highlight.js.

I'll need to get node.js installed - OR I can try to upload highlight.js by itself. Will try the latter first, as it will give more control overall.

I ended up importing highlight.js via a CDN. I won't be changing the version number of highlight.js any time soon, so this should be safe. Maybe consider downloading highlight.js into the public directory.

I then wrote some custom css and javascript:
- CSS to show the code is interactable
- javascript to copy text to clipboard on click

*Finish time:* 00:09