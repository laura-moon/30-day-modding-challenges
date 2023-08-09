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

### Day 8
Generated some more audio and wrote script for introductory scene.

### Day 9
Reclipped audio for CFF using [this guide](https://wiki.beyondskyrim.org/wiki/Arcane_University:Voice_Line_Implementation) - added to Data folder and regenerated lip files.
Generated audio for introductory scene.

Next steps:
- Generate, clip and add in greeting lines (follow Joseph Russell tutorial #4 - [Saying Hello](https://www.youtube.com/watch?v=ycX2QWI08ls))  
- Implement introductory scene [using this video](https://www.youtube.com/watch?v=iFDZjhVxaSg)
- Refine appearance
- Watch [this video on AI packages](https://www.youtube.com/watch?v=A4T7iNO5YKg&list=WL&index=1&t=1s)
- Add conditions so his College travel and sandboxing packages don't fire until after MQ01 stage 30
- Add in replacement AI packages to keep him busy in the meantime

## Reboot
I ended up taking a break from working on Alex.  I did pick things up again, but forgot about updating this log for a while.  I'm piecing this together from my commit history.

I followed the introductory scene tutorial.
I'm waiting for Elevenlabs to release their STS but used temporary lines to get everything working.

### Reboot Day 1
I followed JR's tutorial to get greeting lines added.

### Reboot Day 2
I started implementing the fetch quest.  Created tome of enchantment and added it to Geirmund's Hall - I was trying to avoid dungeons that are associated with either the Main Quest or the Faction Quests, and this is a nice location.  I placed it somewhere that the player could just grab it and go, but if they did want to explore further, they could end up starting a cool quest.  I used [this video](https://youtu.be/G6QbxZSgyxA) for creating the book, especially how to add the cool illuminated letters. 

### Reboot Day 3
I went through and found the best of the lines I had generated that could be used as temporary audio for the introductory quest.  I also recorded myself saying the lines - I will use these tracks to generate the actual lines once the STS feature is launched.

### Reboot Day 4
I added all the dialogue for the initial conversation, and scripted to progress the quest onto stage 10 - I followed [this video](https://youtu.be/iFDZjhVxaSg) and started adding scripting to progress the quest stages through dialogue.

### Reboot Day 5
I used [this tutorial](https://www.creationkit.com/index.php?title=Bethesda_Tutorial_Basic_Quest_Scripting) to add a script to the book so that when the player adds the book to their inventory, the quest stage is progressed and the new quest objective is displayed.  This took a lot of time to get working and I'm still not sure what I was doing wrong.  In the end I got it working through using the code from [this page](https://falloutck.uesp.net/wiki/OnContainerChanged_-_ObjectReference) instead.  The only difference I can see is that the second one uses akNewContainer and akOldContainer rather than newContainer and oldContainer.  I don't know enought to tell if this could make a difference or not, but whatever, it's working now.  I also changed the Follower Quest so that will not start until the Introduction Quest is completed - I've not checked that this works yet as I still have to implement the final part of the fetch quest, which will complete that quest.

### Reboot Day 6
So far my intro quest has been set to Start Game Enabled, and I used [this tutorial]() to generate a seq file.  I have seen a few people say that it's not best practice to have these sorts of quests as start game enabled and in any case there is no need for this one to be, as there's no way that you can talk to Alex until you visit Winterhold.  My initial thought is to set it so that entering the Arcanaeum will trigger it, but that would force you to do either CoW or Main Quest... but then the whole thing is that you're in the Library looking for a book, so I suppose that is okay.  If I did go on to reworkd the mod to release I would probably completely change the introductory quest in any case.  I can think about that later.  For now I will use [this tutorial](https://www.creationkit.com/index.php?title=Bethesda_Tutorial_Story_Manager) to change the trigger for the quest to be Change Location Event with the player entering the Arcanaeum.  
Okay, so the tutorial linked above uses a scripted event to trigger the scene and I decided to go for a simpler change location event.  I couldn't find mucj info on how to do this, the only tutorial I could find was [for Fallout 4](https://youtu.be/DlMYJ-QcyiQ) but it seems to work.  
The only thing is that now my quest and map marker for retrieving the book aren't working... Take a break and try to fix that before moving on.

I also need to finish the dialogue for the fetch quest - I haven't implemented the lines for when you return the book to Alex, and I need to think about how to handle him teaching you new enchanting techniques.  I'm thinking maybe a fade to black then after that the player's enchanting skill gets incremented. 

### Reboot Day 7
I finished the dialogue for the fetch quest with temporary dialogue - I'm waiting for ElevenLabs to release their Speech to Speech conversion before I generate any more lines.  I also made a patch that hooks into ostim's kissing animations, triggered by dialogue.  I used the instructions from [this mod](https://www.nexusmods.com/skyrimspecialedition/mods/97073) 

### Reboot Day 8
Got back on the AI horse.  Started simple with vanilla eat, sleep and sandbox packages, following [this tutorial](https://www.creationkit.com/index.php?title=Bethesda_Tutorial_Packages).  He still didn't sleep.

### Reboot Day 9
Messed around with his AI packages again and realised that ownership of the bed in the house was set to player bed faction. I changed the ownership to Alex and he went straight to sleep at the start of his sleep package!
