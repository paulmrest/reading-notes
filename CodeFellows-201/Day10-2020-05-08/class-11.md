# Read 11 - Assorted Topics


## Summaries from Jon Duckett's book, "HTML & CSS":

## Chpater 16 - Images

CSS allows images to be resized, taken out of the normal flow, moved around, aligned horizontally and vertically with other elements, and a number of other formatting options.

Addtionally, CSS allows images to be set as a background image, and for that background image to have properties like being static, repeat across the page.

Images can also be used as an effect when the user's mouse hovers over an element, like a button or link.


## Chapter 19 - Practical Information
## Page 476 - 492

**Search engine optimization** (SEO) allows you to tweak your site so that search engine algorithims will move it higher in rank for your desired keyword searches. Things like making sure your site as a page title, a relevant URL if possible, important keywords are repeated throughout the site, and descriptive link text, all help with SEO. Another huge part of SEO is linking to other relevant sites, and getting those sites to link back to yours.

**Google Analytics** is a good tool for learning about your site visitors.

**File Transfer Protocol** (FTP) was (maybe still is, I did some additional research and apparently some hosting companies still use it) a common way for web designers to get their files to teh hosting company.

## Chapter 9 - Flash, Video & Audio
## Page 201 - 206

Flash was a thing. Created in the 1990s, very popular until the early to mid 2010s as a way of displaying video/audio on websites. Quite insecure, and dead now. Replaced by HTML5 and other technologies. Good riddance.

The only great loss is that no one has replaced [Zomobo.com](http://www.zombo.com) with an HTML5 version at that original URL. [HTML5 Zombo.com](https://html5zombo.com/) exists, but it's just not the same.


## [MDN - Video and Audio APIs](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Video_and_audio_APIs)

The HTMLMediaElement API is part of the HTML5 spec, and completely replaces Flash in all modern websites. The API allows a number of controls over how media content is displayed and controlled by the user. Media files are included in the HTML via the `<source>` tag, and players are wrapped in elements, like a `<div>`, so CSS can be used to position and size them on the page.

JS is used to actually access the media files and tell them to play, pause, jump forward and abck, etc. There a number of ways that JS and CSS can be used to customize the control and behavior of media in a browser window.