---
layout: post
title: "Auto Py To Exe"
date: 2018-03-10
categories: Projects
tags: Python pyinstaller Eel GUI
---

* content
{:toc}

This project allows you to convert python scripts to executables with a simple interface. The interface uses chromes app mode and lists all possible flags for pyinstaller.

[Find the project on GitHub here](https://github.com/brentvollebregt/auto-py-to-exe)

## What is this?
This application displays a simple interface that allows you to convert py to exe easily. By just selecting the file, if you want it to convert to onefile and if you want a console, you will only need to press convert and wait for the script to do the rest.

<div style="text-align: center">
	<img src="https://i.imgur.com/EuUlayC.png" alt="Empty interface"/>
	<p>The script is built using <a class="link" href="https://github.com/ChrisKnott/Eel">Eel</a> and uses pyinstaller to convert the script.</p>
</div>

<!-- more -->

## Getting Started
### Prerequisites
- Python : Python 2.7 or Python 3.3+ (basically anything that pyinstaller runs on)
- Chrome : to run the user interface in; eel uses this (app mode)

### Installing 
- Clone/download the repo [here](https://github.com/brentvollebregt/auto-py-to-exe)
- Open cmd/terminal and cd to the project
- Execute ```pip install -r requirements.txt```


## Running the Application
Run ```run.py```. Chrome will open in app mode with the project running inside.

## Using the Application
1. Select your script location (paste in or use a file explorer)          
	- Outline will become blue when file exists
2. Select other options and add things like an icon or other files
3. Click the big blue button at the bottom to convert
4. Find your converted files in /output when completed

*Easy.*

### Passing the File With Arguments
Alternatively you can execute ```python run.py [filename]```. This will open up the window with the filename in the script location.

## Video
If you need something visual to help you get started, I made a video for the original release of this project, some things may be different but the same concepts still apply.

{% include embedYouTube.html content="OZSZHmWSOeM" %}

## Something is Wrong?
There could be a chance that you were using an old version and I have changed something and your cache is now a mess. Press Shift+F5 in the chrome app to force reload everything.
If this doesn't work please [report it](https://github.com/brentvollebregt/auto-py-to-exe/issues) and I will look into it!

## Screenshots
![Empty interface](https://i.imgur.com/dd0LC2n.png)
![Filled out](https://i.imgur.com/Wd9pFqR.png)
![Converting](https://i.imgur.com/MjdONcC.png)

## Response
I really wanted to get this project out there so I released a YouTube video demonstrating how to setup and use the interface (video above). A day later I made a post in the /r/Python sub reddit titled ["Auto Py to Exe is Complete"](https://www.reddit.com/r/Python/comments/84kwb8/auto_py_to_exe_is_complete/).
To my surprisement the next morning (about 7 hours) I had more than 300 upvotes which to me was a big thing. I had many replies which I took time to read and reply to. About 44 hours later the post finally lost it's top place on the subreddit and the post is sitting at 454 points with 12.1k views and 75 comments.
I can't believe how big this got and it means a lot to me when I saw people thanking me for the project. When the couple of issues came to the Github repo I realised people do care about this and I was quick to fix these.
Once again, thank you for the support; I loved making this project.