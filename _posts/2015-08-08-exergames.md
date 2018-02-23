---
title: Exergame
author: Paul
layout: post
icon: fa-lightbulb-o
image: roadrunner.png
---

This project is to create games for elderly. It requires the player to move their body while playing games.
Microsoft Kinect is used to detect body movement. While the game development was done on Unity Engine with C#.  
![Kinect](/assets/images/kinect.png){:.center-image height='30%' width='30%' }

Microsoft did a great job providing [toolkit](https://www.microsoft.com/en-my/download/details.aspx?id=40276) for the beginner.
But this [gentleman](https://assetstore.unity.com/packages/tools/kinect-with-ms-sdk-7747) brings the toolkit to another level. He actually wrap the
code and allow kinect to works on unity itself. So all I did was create gesture that I want as game input while maintaining the
game logic.

### General idea
The idea is to use kinect framework to detect the skeletal system and translate it into the movement or action of humanoid model.  
![howkinectwork](/assets/images/how-kinect-works.png){: .center-image height='50%' width='50%'}

### Posture
Posture and gesture are different. Posture is consider static while gesture are series of posture.  
![posture](/assets/images/posture.png){: .center-image height='50%' width='50%'}

### Gesture
![gesture](/assets/images/gesture.png){: .center-image height='50%' width='50%'}

### Home Screen
This is where you get to choose which games you wanna play. Player needs to move their hand around the button and grab their fist to select.  
![menu](/assets/images/menu.png){: .center-image height='50%' width='50%'}

### Road Runner
This games aims to train elderly of their body gesture and balancing. (Never even been tested on elderly.. Argh !!).
The player use posture and gesture listed above to control the humanoid model. The games works exactly like subway surfer.
The model will keep on running, and if he hits banana. The time extent. Alcohol bottle gives time penalty. When the times is up. player lose the game.
If player manage to survive after a time frame, there will be a change in scene. Game logic changes to slightly harder mode. (Told you its not for elderly.. lol)
![road-runner](/assets/images/roadrunner.png){: .center-image height='50%' width='50%'}  

### Step game
This game utilize only the lower part of body. If you are old enough like I do, u might play with PlayStation dance pad before except
that the pads are all in virtual world. It again aims to improve the balancing of elderly (which apparently never have been tested). Besides,
it also track the reaction time and movement time of the player's leg  
![step-game](/assets/images/stepgame.png){:.center-image height='50%' width='50%'}

Video and some explanation on game logic.

<iframe  class='center-image' height='50%' width='50%' src="https://www.youtube.com/embed/_qdYr6-pz-w?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

### Some extra ideas
I found something called skanect that allow the user to scan the human body and produces a 3D mesh of the model. Its free, but has limited number of vertices.
I then threw in the .obj file (That 3D model created by skanect) into Blender and used blender builder function 'Bisect' to cut the waist into half. Blender is so powerful
that you could actually write code on it. Its like Windows Paint that could actually do C++. Hence. I copy some unknown code online (TY the author i have no idea who).
The code works fairly simple, it calculate the distance between each vertices that I 'Bisect'ed and sum up the result. And you know what I get? The waist circumference.
Imagine how this idea can be achieved in cloth industry. Enough talk. Lets see the result. And Yes, that is me. Naked for science.  
![blender-body](/assets/images/blender-body.png){: .center-image height='50%' width='50%'}
Yes. My waist was 71cm that time. Good old time Huh ? I couldn't remember the accuracy well (+-2cm?). This is just some extra thing I did just because it looks fun & cool.  
![blender-result](/assets/images/blender-result.png){:.center-image height='50%' width='50%'}




source-code: [here](https://github.com/aapaulng/exergames)
