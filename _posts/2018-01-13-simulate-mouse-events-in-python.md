---
layout: post
title: "Simulate Mouse Events In Python"
date: 2018-01-13
categories: Youtube
tags: Python Mouse pynput
---

* content
{:toc}

This demonstrates how to control the mouse with Python. Using pynput we are able to simulate mouse events into any window. This will show you how to press buttons, scroll and move the mouse.

{% include embedYouTube.html content="2BXr9U6ZL8Y" %}

<!-- more -->

## PIP
If you haven't used or setup pip before, go to my tutorial at [{% link _posts/2017-12-13-how-to-setup-python's-pip.md %}]({{ site.baseurl }}{% link _posts/2017-12-13-how-to-setup-python's-pip.md %}) to setup pip.

## Installing Pynput
We will be using the punput module to listen to mouse events. To install this module execute ```pip install pynput``` in cmd. Watch the output to make sure no errors have occurred; it will tell you when the module has been successfully installed.

![Installing pynput](/images/how-to-get-mouse-clicks-with-python-pynput1.png)

To double check that it was installed successfully, open up IDLE and execute the command ```import pynput```; no errors should occur.

![Testing pynput](/images/how-to-get-mouse-clicks-with-python-pynput2.png)

## Simulating Mouse Events
Create a new script and save it somewhere so you can easily run the script. Import Button and Controller from pynput.mouse.

```python
from pynput.mouse import Button, Controller
```

Make a variable called mouse and set it to an instance of Controller. Now using the mouse variable we can control the mouse.

```python
mouse = Controller()
```

### Finding the Position of the Mouse
To find the position of the mouse we can use mouse.position. This will return a tuple of two integers. The first integer is the x position and the second integer is the y position. This is relative to the top left of the screen; x getting bigger is going right and y getting bigger is going down.

```python
print ("Current position: " + str(mouse.position))
```

### Setting the Position of the Mouse
To set the position of the mouse we can use mouse.position again. By setting this to an x and y point, the mouse position will be updated immediately.

```python
mouse.position = (10, 20)
```

### Moving the Mouse Relative to it's Position
Instead of getting the mouses position and calculating where it needs to be moved to if you want to move it a distance relative, we can use mouse.move. Passing an x and y integers to this will move the mouse relative to it's current position. For example, if I wanted to move it to the right by 20 pixels and up by 13 pixels, I would use:

```python
mouse.move(20, -13)
```

### Clicking Buttons on the Mouse
To click buttons on the mouse, we would use mouse.click. Passing a button from the Button class imported and an integer, we can preform single, double and triple clicks for any button.

```python
# Click the left button
mouse.click(Button.left, 1)
# Click the right button
mouse.click(Button.right, 1)
# Click the middle button
mouse.click(Button.middle, 1)
# Double click the left button
mouse.click(Button.left, 2)
# Click the left button ten times
mouse.click(Button.left, 10)
```

### Pressing and Releasing Buttons
We can also click a button using press and release methods. This would also allow us to drag an object by pressing, moving and then releasing. To press we would use the mouse.press method and to release we would use the mouse.release method. Both these methods need a button passed which can include the left, middle and right as shown above. More buttons can also be included depending what operating system is being used.

```python
mouse.press(Button.left)
mouse.release(Button.left)
```

### Scrolling
To scroll we need to use the mouse.scroll passing two integers for horizontal and vertical scroll. The first integer is for horizontal which is left to right scroll; a positive integer will scroll right vice versa. The second integer is for vertical which is up to down scroll; a positive integer will scroll up vice versa.

```python
# Scroll up two steps
mouse.scroll(0, 2)
# Scroll right five steps
mouse.scroll(5, 0)
```

Depending on your mouse settings, you may need to use bigger step values to see movement in the scroll. I have witnessed this myself and sometimes may need to use around 100 steps to move my mouse.
## FAQ