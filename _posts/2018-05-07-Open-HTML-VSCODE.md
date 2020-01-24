---

firstPublishedAt: 1525677890635
latestPublishedAt: 1525677890635
slug: opening-your-html-code-through-vs-code
title: Opening your HTML code through VS Code
tag: Programming
---

Being a past Sublime PC user, I would right click the html file and select **Open in Browser**. Pretty simple. However, now I would like to go through this process in VS Code.

How would I open HTML code from VS Code into my web browser, particularly Google Chrome?

Well, boy oh boy, here is the solution for you, [provided in this article](https://www.webucator.com/blog/2016/06/launch-files-browser-visual-studio-code/):

1. Open VS Code

1. Enter CTRL+Shift+P

1. In the opened pallette selection, enter in **Configure Task Run**

1. You will then click **build,** in which a* task.json *file will appear.

1. Replace the text with the following:

![Json Object seen below (image from stack overflow link, below](https://cdn-images-1.medium.com/max/1198/1*gwNP2uMg1dqbctBa_uRuOw.png)

> {

> “version”: “0.1.0”,

> “command”: “Chrome”,

> “windows”: {

> “command”: “C:\\Program Files (x86)\\Google\\Chrome\\Application\\chrome.exe”

> },

> “args”: [“${file}”]

> }

[Stack Overflow Link to “How to View HTMl Code in Browser](https://stackoverflow.com/questions/30039512/how-to-view-my-html-code-in-browser-with-visual-studio-code)

6. Save the task.json file

7. Enter CTRL+Shift+B (Similar to that of Sublime Text) [It’s okay to re-load]

And presto! You are done.

Cheers,

Raul Maldonado

_Note: Mac user editing can be found in Stack Overflow link above, after raw json code._
