This document is a guide for the drive train for those who are not well versed with the driver station, control hub, and software.

I will be assuming that you have **ZERO** knowledge prior to reading this document. If you happen to know some of the topics I cover, you are free to skip them.

# Hardware/Firmware
This section will deal with the physical aspects of the robot. We will talk about the driver station, control hub, battery, and expansion hub (if you have one).

### Components
---
<br>

**On your robot you should have at the bare minimum:** Control Hub, Battery <br>
**Additional Hardware:** Expansion 

### Powering on the Robot
---
<br>

Your control hub WILL have a power cable. One side will be connected to a plug labeled **BATTERY** and the other side should be unplugged.<br>

Your battery will also have a cable coming from it. It is also unplugged. Plug the two unplugged sides together. Your control hub, and expansion hub if you have one, **should now have a light show up.**

This light should initially be blue. The control hub's light will than switch to green if the control hub has successfully powered on. 

> You may notice your expansion hub does not turn the color green. This is fine, as we need the control hub to turn green.

> If the control hub does not turn green and either stays blue or turns some other random color, go search up how to troubleshoot it.

### Connecting the Driver Station to the Control Hub
---
<br>

Grab your driver station device and go to the FTC driver station app. Hopefully you are on a screen with a large "**INIT**" button.

> If you are on a screen that does **NOT** display what I just described, go find a consultant.

First, look to the top of the screen. In the top left you will see the FTC logo and, to the right of it, either "**Robot Connected**" or "**Robot Disconnected**". The former means that the robot is online and connected to the driver station, the latter means the opposite.

I will assume that the robot is not connected.

> If the robot IS connected (somehow), skip this section and go to "**Configuring the Driver Station**"

In the top right right, you should see a bunch of diffferent things. From the left most to the right, you will see: <br>
* Network: [network name]
* Ping: [ping in ms] - [channel number]
* Wi-Fi Icon
* User 1 with a controller icon
* User 2 with a controller icon

Tap on the 3 dots in the top right (they are position in a column). You should now see a drop down with many different options. Select "**Settings**".

You will see, again, a lot of different options in the "**Settings**" page. Look for the one that says "**Pair with Robot Controller**". It should now bring you to another page, where the most important part is the part that says "**Current Robot Controller**". Under that should be a network name. Under the network name should be a button that says "**Wi-Fi Settings**"

I will assume you are **NOT** automatically connected to your robot. However, if the driver station device has previously been connected to the control hub, it should auto-reconnect. Check the network name, it should be "**TeamNumber-RC**".

Tap on the button, it will bring you to the Wi-Fi page. On this page search for the robot's network, assuming the robot is online. You are looking for a network that follows this name: "**TeamNumber-RC**"

Once you find it, connect to it and it will prompt you for a password. The password to Arrowhead's network should be "**arrowhead**" (Yes, it's case sensitive).

> Can't find your network? Maybe the robot's network changed to default. If you cannot find it, find a consultant ASAP.

> Found your network, but the password doesn't work? Find a consultant who has REV Hardware Client installed. They will be able to change the password. The password may have also switched back to the default password. The consultant will know what that is.

Once you are connected to your robot's control hub, great job! You are now done connecting the driver station and the control hub. You may now proceed to the next section.

### Attaching Peripherals
---
<br>

Short section. Look at the bottom of the driver station and you should see a few ports. One particular one, USB-C, is named battery because this is the USB port you use to charge your driver station. 

You should see 3 USB-A ports. This is where you want to plug in your controllers. This will be a simple process, find the USB coming off of the controller and simply plug it into the driver station's USB-A ports.

>If your controller is plugged in, however does not seem to work, plug the controller into another port. Some ports may simply not work with some controllers, which means the driver station will not take inputs (very bad).

### Configuring the Driver Station
---
<br>
Before you initialize the robot (The big INIT button stands for initialize), you must first enable a configuration.

Again, tap on the 3 dots in the top right. Look for the button that says "**Configure Robot**" and tap it. You should now see a list of available configurations.

Under each configuration's name, three buttons appear. They work as following:
* **Edit** - Allows you to edit the configuration.
* **Activate** - Activate the configuration to be the active configuration.
* **Delete** - Deletes the configuration.

There will also be the button in the top left labeled "**NEW**". It does as expected, and will allow you to create a new configuration from scratch.

I will be ignoring this aspect of configuring the robot. There should already be one, or more, configuration(s) on the robot.

In our case (Arrowhead), I have created two configurations. One is named "**Comp3_TeleOp**" and the other is "**Auton_Tuning**".

> Ignore "**Auton_Tuning**" as that is a developer configuration and should not be used in this following competition.

Activate "**Comp3_TeleOp**". Now go back to the home screen of the driver station. You should see the robot restart itself. That's normal. Once it's done restarting, we are done with configuration.

# Software

This section will now go in depth about the software side of the robot. We will be working with the driver station, the control hub, and the Java files.

### Initializing the Robot with a File
---
<br>

Go to the homescreen of the driver station app, which contain a large INIT button. Now, look above the INIT button you should see 2 dropdown arrows with text in between them that says "**Select OpMode**". Under this text, you will see arrows that point to both dropdown arrows, which label what they do.

Tap on the dropdown arrow on the right, which has an arrow pointing towards it aptly labeled "**TeleOp**".

You will now see a a screen with a bunch of names, on a white background (hopefully I have remembered it correctly). This is good, you are on the right track. Find the file you want the robot to run, for Arrowhead this file is: "**Field Centric Driver Control (TeleOp) :D**" (Yes, there is a smiley face in the name... that's intended).

Once you tap on the name, it should load the file and return back to the home screen.

Congratulations! You have now initialized a TeleOp file into the control hub of your robot.

### Running your Robot
---
<br>

Assuming you have followed all previous steps in chronological order, you should have just finished initializing a file into your robot.

You're almost there. Just a few more steps.

Press the INIT button. The button should now turn into a triangle. This triangle means that the file is paused right now.

Press the button with the triangle and you should see it change to a square. Your robot is now running the file that you have initialized. You should now be able to control your robot with your controllers.

Oh yeah, about that. I haven't taught you how to activate your controllers. The reason I haven't done so is because I would rather prefer you activate them when the robot is about to start running.

Don't worry, it's simple. Grab the controller you want to be controller 1. Now press the "**start**" button and "**X**" button at the same time. You should see the controller icon above "**User 1**" light up, which signifies that you have successfully paired controller 1.

The same procedure can be repeated for controller 2, with one exception. Press the "**start**" button and "**A**" button. This should now light up the icon for "**User 2**".

>If you find that this doesn't work, find a consultant. I'm writing this based off memory.

# Miscellaneous

This is where I will add additional information

### ______ doesn't work?
---
<br>
As I have stated multiple times in this manual, the best course of action is too simply find a consultant.

### Field Centric isn't working?
---
<br>
I predict this will be a problem. Don't worry, it's something to do with my code. For now, do the following: <br>
<br>
Make sure the robot is not moving. Simplest way of doing this is to pause the file, if it's running.

Now move the robot to where you want it to start at the beginning of driver control period. Ensure the front of the robot is facing away from you. For Arrowhead, this is the side with the slides extruding outwards.

Now, tap on the 3 dots in the top right to open the drop down. Find the option that says "**Restart Robot**", or something along those lines (remember, I'm writing this from memory). 

Once the robot has finished restarting, open the file dropdown and select the file you want to run. Press the INIT button to... initialize the file.

Now when you start running the file, the robot should now be field centric relative to where the robot was facing in the north direction, also the front.

> **Do you not have an autonomous?** Then it is recommended that this restart of the robot is not done in the seconds prior to driver control period, or when driver control period start. Please do this during autonomous or prior to the match starting.

> **Do you have an autonomous?** Then... I actually don't know since Arrowhead does not have an autonomous. For now, ignore this part of the manual until I have successfully tested this scenario out.

