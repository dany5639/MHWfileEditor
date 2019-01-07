# MHWfileEditor
All files uploaded here are property of Monster Hunter World creators.

WARNING: use these instructions or files at your own risk. I never had issues with the game or savefiles during my tests.

// How to remove or replace Xeno effects that freeze the game. Potentially works with any other freeze caused by specific events.
Extract all files with WorldChunkTool.
Find the extracted file "chunk5/em/em105/00/epv/em105_00.epv3" .em105 is for Xeno.
Create the missing folders to copy it to "Monster Hunter World/nativePC/em/em105/00/epv/em105_00.epv3"
Open em105_00.epv3 with a hex editor, I recommend Hex WorkShop.
Find all of the following strings and either replace them with any other string to replace the effect, or replace the string characters to prevent the game from reading it.
em105_00.epv3 basically points to other effect files, specifically efx files, which cause the freeze when they are rendered.

vfx\efx\em\em105\em105_001
vfx\efx\em\em105\em105_006
vfx\efx\em\em105\em105_018
vfx\efx\em\em105\em105_021

// How did i find which effects crash
If you finished the main quests, you beat Xeno and the cinematic is in the gallery, title menu.
In the extracted files, chunk0\event\evc0067\evc0067.sdl is the file for the last Xeno cinematic.
Copy it to nativePC\event\evc0067\evc0067.sdl and open in the hex editor.
At the end of the file, all used effects are listed. Simply replacing a few with one effect at a time will show which effect starts freezing. 3rd and 4th effects are left and right arm effects, 5th 
renders when it fires it regularly from the mouth.
These changes also reload when you replay the cinematic, very useful to quickly change effects and test.
All the effects used by Xeno during gameplay are listed in em105_00.epv3.
