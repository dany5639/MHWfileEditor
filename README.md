All files uploaded here are property of Capcom. They can also be extracted from the game by any game owner with public open source tools.

WARNING: use these instructions or files at your own risks. I never had issues with the game or savefiles during tests.

The uploaded files should completely remove any effects that freeze the system when Xeno fires his lasers.
Exemple of a correct path "C:\MHW\nativePC\em\em105\00\epv\em105_00.epv3"
The default file is required if you want to add back or remove other effects.

How I removed Xeno effects that freeze the game. Potentially works with any other freeze caused by specific events.
1) Extract all files with WorldChunkTool.
2) Find the extracted file "chunk5/em/em105/00/epv/em105_00.epv3" .em105 is for Xeno.
3) Create the missing folders to copy it to "Monster Hunter World/nativePC/em/em105/00/epv/em105_00.epv3"
4) Open em105_00.epv3 with a hex editor, I recommend Hex WorkShop.
5) Find all of the following strings and either replace them with any other string to replace the effect, or replace the string characters to prevent the game from reading it.
6) em105_00.epv3 basically points to other effect files, specifically efx files, which cause the freeze when they are rendered.

vfx\efx\em\em105\em105_001
vfx\efx\em\em105\em105_006
vfx\efx\em\em105\em105_018
vfx\efx\em\em105\em105_021

// How did i find which effects crash
1) If you finished the main quests, you beat Xeno and the cinematic is in the gallery, title menu.
2) In the extracted files, chunk0\event\evc0067\evc0067.sdl is the file for the last Xeno cinematic.
3) Copy it to nativePC\event\evc0067\evc0067.sdl and open in the hex editor.
4) At the end of the file, all used effects are listed. Simply replacing a few with one effect at a time will show which effect starts freezing. 3rd and 4th effects are left and right arm effects, 5th 
5) renders when it fires it regularly from the mouth.
6) These changes also reload when you replay the cinematic, very useful to quickly change effects and test.
7) All the effects used by Xeno during gameplay are listed in em105_00.epv3.
