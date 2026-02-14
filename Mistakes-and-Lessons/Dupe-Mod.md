# Minecraft Duper

This is a recollection of something that happened about 3 months ago (mid-late 2025), so my information may not be totally accurate.

This piece of malware was also documented on a youtube channel by the name of Eric Parker: https://youtu.be/-pwgNDCS6QM?si=XRfIfQH___k2h8QL

## Setup and Execution

This story comes from when I was experimenting with Minecraft duplication bugs. At first I was using a legitimate tool know as UIUtils to try de-syncing bugs, to no avail. I then tried looking to youtube tutorials for dupe finding and found a video with a title similar to this: "UNIVERSAL Minecraft Dupe! (Working as of 1.21.11)". The video showcase a person executing the "dupe" by dropping an item and typing ".dupe" into the chat. Once the "dupe" was complete he showed that he used a mod from a website along the lines of dupetoolskit.com and I followed to that website. The site looked well put together with a link to the tutorial I was watching previously. I downloaded the file and saved it to my fabric mods folder. However, when I ran minecraft and started testing, nothing happened. I figured this was due to UIUtils also being installed. So, I deleted UIUtils and tried again, this obviously didnt work. I quit minecraft and saw this flag from my BitDefender AV "Suspisious file detected at C:\Users\Andrew\AppData\Local\Temp\mal.bat".

## Response

I first deleted the mal.bat file my AV had quarantined and the "dupe" mod. I then researched on reddit for what to do in case it was a RAT. I got mostly two answers, AV scans and checking startup programs. First, I went and cleared out my TEMP folder in case there were any remnants of the malware still there. Then I ran a full AV scan with both BitDefender and Windows Defender. As those scans were running I went into task manager and removed all apps I wasn't familiar with and were not crucial to start up (checking each process with google). The scans finished, coming back with no detections. The next day I ran another scan to make sure it wasn't missed or the payload was delayed, which also came back with no detections.

## Red Flags

### UNIVERSAL DUPER

This was a red flag because minecraft is a very bug resistant game, and "universal" dupes are few and far between and often get patched very fast. Most dupes are with server plug-ins that are separate to the game.

### Separate Mod

Most dupes are executed with no mods at all, UIUtils, or custom scripts developed by bug hunters. Another separate mod like this one is very rarely needed for a dupe.

### Previous Experience

This is only isolated to me. I had watched a video earlier that year with the EXACT piece of malware that I had downloaded (Eric Parker Youtube: https://youtu.be/-pwgNDCS6QM?si=XRfIfQH___k2h8QL). This should have been in my memory that people were using minecraft mods to hack systems.

## Lessons

### Unstrusted Sites

When installing minecraft mods, only install mods that are well trusted with the minecraft modding community. Never install mods from untrusted distribution sites, the main mod sites are CurseForge and Modrinth.

### Persistance

If a tutorial or instruction online tells you there is only ONE specific way to do it, also take extreme caution. For example, phrases like "This is the only..." or "Download from this site..." are very common for malware examples.

### Isolation

If there is a tutorial for something major within a community but there isnt very much talk in the community about said tutorial, it is probably fake. For this example, a "universal" dupe is very serious within the community and would spread around very fast.

### Comments

On a tutorial posted to a site that allows comments, check them!. Common comments on malvertisment tutorials often point out flaws you didn't see or outline their own experience with that malware.

### AV

You need to have a good antivirus always, from what ive heard bitdefender is the best free antivirus (but make sure to do your own research). In this example, BitDefender was able to stop the mal.bat file from executing.