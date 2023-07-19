### Day 1 
Created the NPC record following Joseph Russell's Tutorial #1 - [Starting with Vanilla](https://www.youtube.com/watch?v=oJB7eLcCo0c).  
Created face for him in RaceMenu.    
Exported nif and texture for face.

### Day 2
Finished NPC record using YoungMaleEager voicetype.  
Attempted to update appearance to the one I created.   
Could not resolve dark face bug - try again tomorrow.  
Also I think I am going to do custom voice type rather than use YoungMaleEager voicetype.  
Added Quaint Shelter as a master and gave Gwilym ownership of it.  
Generated a load of audio with ElevenLabs.

### Day 3
Restarted entirely.  NPC is Alex, he just won't be called anything else.  This is just for me, save Gwilym for if I ever make a mod to be released publicly.  
Fixed appearance - there was something wrong with the beard I was using.  
Followed Joseph Russell tutorial to create custom follower framework  - Tutorial #2 - [Creating a Custom Follower Framework](https://www.youtube.com/watch?v=kEVu-ujB9XU&t=2189s)  
Spent at least an hour trying to work out why the script I had copied and pasted from JR's website wouldn't compile.  Turned out my CK prefs ini was looking for scripts in Source/Scripts rather than Scripts/Source.  Did also figure out how to use the Pyro stuff in VSCode though.  
Followed Joseph Russell tutorial to create custom voice type and start adding audio files - Tutorial #3 - [Recording and Editing Voice Audio Files](https://www.youtube.com/watch?v=aWvnr05bXbQ&t=674s).  
Started clipping audio files (or not, as it turned out).  
Merged appearance records into main plugin rather than as separate overwriting plugin.  Broke appearance in the process.

### Day 4
Fixed appearance, again.  
Reclipped audio files (I had incorrectly exported all the files I did yesterday, exporting the whole file rather than the selection).  
Attached audio files for the dialogue lines I added yesterday and generated lip files.  
Tested in game, all working as expected.  
Clipped more dialogue lines for greeting, in preparation for next Joseph Russell tutorial.
Discovered that I've cut all the dialogue lines to short so I'm going to have to do them all again. 
Started messing around with AI packages using [this tutorial by Darkfox127](https://www.youtube.com/watch?v=E3Nd8LXYRA0&t=900s) and (the Creation Kit wiki)[https://www.creationkit.com/index.php?title=Category:Packages#Package_Templates]
Plan - travel package to College, sandbox package for College Arcanaeum, travel package to Frozen Hearth, sandbox packaged at Tavern, travel package to Quaint Shelter (his home), sleep package at Quaint Shelter, default sandbox package at Quaint Shelter.
I initially thought that he got stuck at the College gate which is locked prior to the player joining the quest, but in fact his travel package, which I had set to 2 hours, ran out just inside the gate.  I ammended it so it was 4 hours which got him to the College but he just stood there, just inside the door, until the travel package expired.
When the sandbox package kicks in, he doesn't do the idles I set in the Package, he just bounces around from chair to chair.  Sometimes it looks like he's starting the animation, but it only lasts for a second or so then he stops.  Not sure what's causing that or how to resolve it.
Also, the gate is still an issue because when he leaves the Arcanaeum to go to the tavern he gets stuck there.
I resolved this by using player.setstage MG01 30 to open the gate.  He did then go to the tavern, but he entered by walking through a wall, and then he stood doing nothing for hours and was not able to leave.  
My plan is to set conditions on the AI packages so he only goes to the College after the player joins, to avoid this issue, but I want to make sure the packages work before implementing that condition and creating new packages for him to use prior to that happening.
I also changed the setting for the Arcanaeum sandbox so that he wasn't allowed to sit down... that did make him more likely to play the idle animations but I feel a bit bad about it lol.

### Day 5
Bad day.  I messed with his AI packages and things got even worse.  I changed the travel packages to travelandplayidles but that didn't seem to make any difference.  He didn't leave the pub.  He just stood in a corner for hours looking like he was attempting to do the idles and not doing the idles.  I got very disheartened at this point but very kind supportive words from the mod makers of the Kaidan EE Discord server perked me up again. 

### Day 6
I intended to take a little break from Alex but woke up motivated to try again, so I did.  I added xmarkers to the Arcaneaum and the Frozen Hearth and directed his travel package to them instead.  I think I need to change the radius (I left it at 0 to see what that would do) because when he got there he just stayed on the marker for the duration of the travel package, which was not my intention.  But, I did have success in that he actually used some of his idles in the Frozen Hearth, after his travel package expired.  Also, some weird stuff was happening and I'm not sure if that's due to my not having saved the game (just coc from the main menu) so I'm going to create a clean save without him installed, and add him to that each time I make changes.  For example, he did not leave the Frozen Hearth at 10pm like he's supposed to.  I the saved the game for the first time and reloaded, and he had disappeared from the Frozen Hearth and was at Quaint Shelter when I went there.  So I'm not sure what would have happened if I had saved the game earlier.  I will test that out later.  Also he was using the idle markers that are placed at Quaint Shelter perfectly, so I want to try adding those in and removing the idles from his AI package to see if that works better. 
 He did not go to sleep.  Try specifying the bed in his AI package.   

### Day 7
More tweaking of his AI Packages.  At the Arcanauem, I added a couple of idle markers and removed all the idles from his AI package as they weren't working properly.  I also changed ownership of one of the chairs so it belongs to Alex, hoping this would make him prefer this one and stop bouncing around all day, but it did not.  Changed radius of xmarker to 250 to see if this would help with him standing stationary when he arrives.  It did not.
Shortened travel time to Frozen Hearth so there would be less time standing still on the xmarker.  This did not work.  
Changed the sleep package so it targets the bed specifically rather than all beds in the cell (there is only one though) - this did not work.  The man will not sleep.
I didn't remove the idles from the Frozen Hearth sandboxing package and these seem to work, I'm not sure why they work here and nowhere else.

Next steps:
- Move on to reclipping audio, and adding in those lines (follow Joseph Russell tutorial #4 - [Saying Hello](https://www.youtube.com/watch?v=ycX2QWI08ls))  
- Write dialogue for introduction scene and create that [using this video](https://discord.com/channels/959790733336936508/963797617127591976/1130256657344114699)
- Watch [this video on AI packages](https://www.youtube.com/watch?v=A4T7iNO5YKg&list=WL&index=1&t=1s)
