# 30 Days of Modding Challenge - NPC Modding

## Anti perfectionism note to self...
This is not an attempt to create the next great NPC.  It is not a creative writing project.  I am not aiming for perfection.  It is a learning project to give me a
variety of tasks in the area of NPC modding, get a taste for whether I want to explore it more in the future, and get some hands on experience writing scripts. 
I am not intending to publish this.  I do not need to appeal to anyone other than myself.  I do not need to be Jane Austen.

## Create NPC
NPC is male Breton called Gwilym.  He is a mage who specialises in enchanting.  He is informally associated with the College of Winterhold.
He will use Young Male Eager voice type.  
- create NPC - follow JR tutorial
- create appearance in Racemenu and add to plugin - follow Van's YT video on NPC replacer and LLewellyn's PDF tutorial on same

## Give Gwilym a house
He lives in Quaint Shelter, just outside Winterhold.  
- add Quaint Shelter and give ownership to Gwilym

## Give Gwilym AI package
Ideally he will have AI package so that he travels to CoW Library where he can be found during the day.  If it's possible (I have no idea what is possible at this stage)
I would like to add some sort of randomness to his evening routine so sometimes he will be at the tavern and sometimes in his house in the evenings.  Usually he will be reading, 
wherever he is.  Or writing, if that's possible???  
?? What else is posible with AI packages?  
- Add AI packages [Darkfox127 AI Packages Tutorial](https://youtu.be/E3Nd8LXYRA0) and [Creation Kit Wiki](https://www.creationkit.com/index.php?title=Category:Packages)


## Introduction quest
Location will be CoW Library.  
Player will approach Gwilym.  Not yet written dialogue.  
- Write dialogue for scene
- Train AI on Young Male Eager voicetype
- Generate dialogue lines needed for these interractions
- Implement dialogue in CK
- Increment player/Gwilym relationship - 1

Result will be fetch quest to find a book about enchantment that a careless student lost some time previously.  
- Create book for fetch quest and place in world somewhere

On returning the book to Gwilym, he will reward the player by training them in enchanting, and the player/Gwilym relationship will increment.    
- Increment relationship ranking - 2
- Increment player's enchanting skill
- ???

## Second quest
This time Alex will approach the player the next time they enter CoW Library
Asks player to gather certain alchemical ingredients he needs for experiment he's working on
??? could have conditional dialogue depending on player's alchemy skill ???
Similar idea to Ingen's fetch quest.  
- Write dialogue for scene
- Generate dialogue lines needed for these interractions
- Implement dialogue in CK

On player's return
- Increment relationship ranking - 3
- Increment player's enchanting skill

## Third quest  
??? Is this too much fetch questing?
Player approaches Alex and asks if there is anything he needs help with.  
Reluctantly he asks for help collecting soul gems that have strong elemental associations - earth (cave) air (mountain) fire (dragon's den) water (lake).  
??? Possibility that he could offer to come with the player for this quest  
- Write dialogue for scene
- Generate dialogue lines needed for these interractions
- Implement dialogue in CK
- Create special soul gems
- Place in world, with quest markers

On player's return
- Increment relationship ranking - 4 (Lover)

Opens up potential integration with Young Lovers mod.

??? How does vanilla marriage work - do I need to do anything or is it automatically an option once relationship reaches 4?







