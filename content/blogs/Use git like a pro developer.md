---
title: Use git like a pro developer.
type: page
# description: Click on me to see the content.
topic: career
author: Noble Varghese
---

Git logs are very basic. 

Let's face it. Git log out of the box is very basic. It throws a bunch of information and we often find ourselves looking confused. It's not very impressive and often filled with information we don't need right now.

Git log with more visibility is what we require. Here is a command that can save a lot of time. 

```
git log --graph --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%an%C(reset)%C(bold yellow)%d%C(reset) %C(dim white)- %s%C(reset)' --all 
```

`--graph` commands let's you add tree structure.
`--format` let's you add custom formats for your logs.
`--all` includes all of the refs, tags, and branches in the logs.

🚀 Attached here is snippet of how the logs look after executing the command.

![Alt Text]("https://noble-varghese.github.io/portfolio/images/screenshot.png" "ScreenShot")