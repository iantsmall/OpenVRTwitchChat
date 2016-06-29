### This is the new home of the TwitchChatOverlay repository!
### It was previously located [over here](https://github.com/Hotrian/HeadlessOverlayToolkit/tree/twitchtest)!
====
This is a stripped down version of the SteamVR Unity Plugin with a custom Overlay script that displays twitch chat!

To use this, Download and launch [the latest release](https://github.com/Hotrian/OpenVRTwitchChat/releases), and enter your Twitch Username, OAuth Key (get your [OAuth Key here](http://www.twitchapps.com/tmi/)) and the desired Channel, then press "Press to Connect" and it should momentarilly connect to your Twitch chat. Check behind one of your controllers (should be left!) for your chat display! It should zoom up when you look at it.

## Features
- See Twitch Chat in VR! From Any Game!
- Easily attach Chat to the Screen, a Controller, or drop it in the World.
- Easily snap Controller attached Chat to a set "Base Position".
- Offset Chat positionally and rotationally.
- Basic Gaze Detection and Animation support (Fade In/Out or Scale Up/Down on Gaze).
- Extremely Basic Save/Load Support! Saves all settings except OAuth Key!

## Basic Controls
(click to enlarge)
![basic controls](http://image.prntscr.com/image/383d945a47b54b1194bf5dd72e9e726e.png)

## Demos
Note that these demos were taken during development, and do not necessarily represent the current state of the branch.
- ![Here is a GIF](https://thumbs.gfycat.com/SinfulHonestGenet-size_restricted.gif)
- Please see this [higher quality view of the GIF above](https://gfycat.com/SinfulHonestGenet) of the Twitch Chat in action!
- [Check out this Youtube Video](https://www.youtube.com/watch?v=JMk7Vy1Zq_s) which shows the desktop UI in action!
- [**Here it is inside TiltBrush!**](https://www.youtube.com/watch?v=tpqIQ5UkGrY) The text is perfectly readable in headset, but seems a little far away on the Display Mirror :P

## Known Issues
- SteamVR_ControllerManager.cs doesn't correctly auto-identify controllers for me, so I wrote my own manager, HOTK_TrackedDeviceManager.cs. My Device Manager is super pre-alpha but should correctly identify both Controllers as long as at least one of them is assigned to either the left or right hand, and they are both connected. If neither Controller is assigned to a hand, they are assigned on a first come first serve basis. If only one Controller is connected, and it isn't already assigned, it will be assigned to the right hand.
- If you launch it and nothing happens in VR, check the Data folder for output_log.txt and look for "Connect to VR Server Failed (301)" if you're getting that error, try restarting your PC, and if that doesn't work [try this solution](https://www.reddit.com/r/Vive/comments/4p9hxg/wip_i_just_released_the_first_build_of_my_cross/d4kmvrj) by /u/GrindheadJim:

>For clarification, what I did was right-click on the .exe file, clicked "Properties", went to the "Compatibility" tab, and checked the box under "Run as Administrator". For the record, I have also done this with Steam and SteamVR. If you're having any issues with any of these programs, I would start there. 

## Additional Notes
- When attaching Overlays to controllers, the offset is reoriented to match the Base Position's orientation. X+ should always move the Overlay to the Right, Y+ should always move Up, and Z+ should always move Forward, relative to the Overlay.
- You can copy and paste your oauth key, you don't have to manually type it out, but you do have to get it off that site, or off another site that generates Twitch OAuth keys.

## How can I help?

If you know how to program, we could always use help! Feel free to fork the repo and improve it in any way you see fit; but if you don't know how but still want to contribute, we always need more beta testers! Download the release and share it around! If you want to do more, donations are always cool too! You'll be funding my programming endeavors, including cool projects like these VR Overlays: [![Donate](https://img.shields.io/badge/Donate-PayPal-blue.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=8PWSSHWNCWWQU)

## Special Thanks

Thanks to Grahnz for the base [TwitchIRC.cs](https://github.com/Grahnz/TwitchIRC-Unity/blob/master/TwitchIRC.cs) script!

Thanks to [Eric Daily](http://tutsplus.com/authors/eric-daily) for the base [SaveLoad](http://gamedevelopment.tutsplus.com/tutorials/how-to-save-and-load-your-players-progress-in-unity--cms-20934) script!

Thanks to everyone who has tested it so far! The feedback has really helped speed things along!