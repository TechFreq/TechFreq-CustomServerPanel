
TechFreq's Custom Server Panel Info Box UI Mod for 7 Days to Die
A modern, clickable, customizable UI experience for modded or vanilla servers.


🧾 Overview
This mod enhances your game’s UI by allowing the user to add custom pause menu panels, such as a custom visuals for the inspect/crafting panel background image, a server join rules dialog background image swap and a customizable pause menu image/ header/title panel— great for community servers, modded experiences, or simply adding quick access links to your Discord, socials, donation page, or modlists.

Latest Changelog:
V1.3 (V2.2)
- Added even more documentation for the server join rules dialog and provided box information , another guide as well as an example for a header image or description box for the pause menu

V1.2 (V2.2)
- Added more documentations towards customizing the server panel info box
- Fixed issue with backpack title or custom backpack header missed the title_key entry as it was just titlekey as it uses localization txt lol

V1.1
- Added new feature for background image for the backpack inventory ui
- Added new feature for custom backpack header or title for inventory ui via localization txt
- V2.2 7D2D


V1.0
- V2.1 7D2D
- EAC Friendly




🧩 Designed to be:
EAC-safe ✅
Server/client friendly ✅

🛠️ Key Features
✅ Pause Menu Enhancements
Custom header image (e.g., your logo or Background)
Up to 5 dynamic buttons linking to external content (Discord, Music, Support, etc vanilla style esque buttons highly customizeable.)
Buttons open the content-hosted XML files via in-game with the built-in NewsWindow format.

✅ Inspect/Crafting Menu Enhancements
Configurable server branding logo while inspecting any item
Configurable Subtitle-style “Welcome” message for immersive flair in this example its welcome to techfreqs inspect panel

✅ Join Rules Dialog
Eye-catching visual and info panel displayed when just before joining a server
Ideal for rules, links, changelogs, Discord, for your image etc.


💼 Use Cases
Discord server invites	Easy-to-click “Join Discord” from the pause menu
Mod links	Players can go right to your modlist from the game
Music promotion	Link to your Spotify / SoundCloud
Donations	Support your PayPal, Patreon, Ko-fi
Rules / TOS	Define server behavior upfront just before joining

📦 Folder Overview
Mods/
└── TechFreqsCustomServerPanelInfoBox/
    ├── Config/
    │   └── windows.xml
    └── ModInfo.xml


🔄 How It Works
🔘 Each button opens an external XML file.

That XML contains a simple <news> block used by 7DTD's in-game news system, like this:

EXAMPLE XML - REQUIRED VIA GITHUB REPO, it can be called Discord.XML but contents inside must be YOUR title for discord and YOUR link.
<news>
  <entry>
    <date>2025-08-09T00:00:00Z</date>
    <title>TechFreq Discord</title>
    <text>Click below to join the official mod server for support and memes!</text>
    <link>https://discord.gg/your-custom-link</link>
  </entry>
</news>

You upload those .xml files to GitHub (as raw links) or any host that allows direct access to the file.
🔗 Set Up Your External XMLs on GitHub
1. Create your XML files:
One XMLper link
Must be simple <news> format

Example filename: Discord.xml
XML
<news>
  <entry>
    <date>2025-08-09T00:00:00Z</date>
    <title>Join the TechFreq Discord!</title>
    <text>Active community and support.</text>
    <link>https://discord.gg/YOURSERVER</link>
  </entry>
</news>

2. Upload to GitHub
Go to your GitHub repo and upload all XMLs:
Discord.xml
Music.xml
Support.xml
Socials.xml
NexusMods.xml

Then copy the Raw links from those xml files:
https://raw.githubusercontent.com/YOURUSERNAME/YOURREPO/branchname/XMLFile.xml

For example:
https://raw.githubusercontent.com/TechFreq/TechFreq-CustomServerPanel/refs/heads/main/Discord.xml

3. Plug those XMLs RAW link into windows.xml for the sources property.

Each button tag will look like this:
<append xpath="/windows/window[@name='ingameMenu']">
    <rect name="btnTechFreqDiscord" depth="30" height="46" width="320" pos="0,-520" anchor="center" controller="NewsWindow"
          sources="https://raw.githubusercontent.com/YOURUSERNAME/YOURREPO/main/Discord.xml">
        <button name="btnLink" hoverscale="1" />
        <label name="btntext" text="Join Discord" />
    </rect>
</append>

🧪 Live Testing
In-game, use the Dev Console:
xui reload from F1 console
To refresh the UI mod without leaving the game.

🧠 Advanced Info
✅ Supported Tags for <news> XML:
Tag	Required	Description
<news>	✅	Root tag
<entry>	✅	1+ required
<date>	✅	Format: YYYY-MM-DDTHH:MM:SSZ (ISO)
<title>	✅	Title for entry
<text>	✅	Paragraph or 1-line message
<link>	✅	URL user can click

🚫 Known Limitations
No direct on_click="openurl()" support	Must use controller="NewsWindow" with external .xml
Google Drive links won't work reliably	Use GitHub Raw, Pastebin Raw, or a CDN
Image aspect ratio matters	If image doesn’t fit right, resize to 1200×1200 or 762×114 for headers or best bet, manually edit the pos 0, 0 positions

Hosted XML deployment via: GitHub
❤️ Support / Share
If you use this mod or learned from this tutorial:
Give TechFreq a shout-out 🎉
Link back to this GitHub/Nexus repo so others can benefit!

🛠 Ready-to-Fork Template
Use TechFreq’s GitHub project:
📂 GitHub: TechFreq-CustomServerPanel as an EXAMPLE please use your own
https://github.com/TechFreq/TechFreq-CustomServerPanel

✅ Fork it
✅ Replace XMLs/PNGS if you wanna be extra
✅ Modify windows.xml
✅ You now have your own custom server panel!


Heavily inspired by other server community's like NAPVP PVP 7D2D Server, TheMeanOnes Relic of Ruins aswell as Eihwaz Custom Panel but not using any assets or materials!




Disclaimer:
By using this mod, you acknowledge that TechFreq is not responsible for any issues, crashes, or conflicts caused by its use.
Use at your own risk. Please backup your game files before installing any type of mod.
Thanks for downloading and enjoy!


Installation:  
Make sure harmony mod exist in the mod directory as it's required.
Download the mod files, Extract Mod files.
Please backup your world, save, and or game files.
Place them in your Mods directory of your 7 Days to Die Game.
EAC must be disabled, although i hope in the future that can be changed, as for now DLLS are not EAC supported however XML has no issue,  this is an XML modification.
THIS IS CLIENT SIDE ONLY but maybe perhaps this is also, server side and client side compatibility?
No further setup needed. Enjoy!


Support Notice:
For those who’d like to support 'TechFreqs' work, This mod may or may not be crossposted. Downloading via 7daystodiemods website through ModsFire (ad-powered, which earns per download) and helps me a ton if posted on there or other example mod sites HOWEVER!
(although its 10 cents per download) There is also a direct mirror for using NexusMods website instead which also features direct links BUT those aren't earned per click or per downloads and run off Donation Points through a different system. The best way to support TechFreq other than downloading mods, sharing the mod with friends, leaving feedback and endorsing the mod in general is all that i ask for, but if you want to go the extra mile although not necessary you may use Donation Links through paypal or ko-fi pages which again helps me a bunch!
However, Donations aren't expected, every little bit of support helps along the way & fuels more mods, music, and bug fixes in the future,so thanks again for reading and being awesome in general and checking out the mod post.





CREDITS:
Thanks to TechFreq & A.I, ChatGPT or Microsoft CoPilot A.I or Grok AI from Twitter or X, for helping me create the modlet, aswell as with very little modding knowledge for the game and learning as i go i couldn't do this without it and overall brainstorming and or the modding community.
I’d very much appreciate it and or any feedback for the mod(s) aswell



Social Media:
If you appreciate 'TechFreqs' work and want to show support, use this donation link, although not necessary.
Kofi Page: https://ko-fi.com/techfreq
I appreciate it in general for just checking out the mod posts, sharing and enjoying any of the mods in itself. Thank you again! and Happy gaming!
Love this mod? Got feedback or ideas or need to troubleshoot?

Join the TechFreq Pretty Rad Squad Discord Server! https://discord.com/invite/SQCnGjNUhw
Chill with us on Discord for game chat, memes, and even more mod updates!
As for TechFreqs music, it's royalty-free music to use in your projects or for casual listening!

Source music files are available feel free to ask away, available in the discord! or for more content! 
TechFreqs Socials: https://beacons.ai/techfreq
Checkout the behind-the-scenes vibes today! Thank you again for checking out the mod post.




License: CC BY-NC-SA 4.0  
This mod is licensed under Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International. You can use it for personal play in *7 Days to Die*. Modifications or sharing require crediting TechFreq, linking to the mod page, and using the same license for derivatives. Contact me at beacons.ai/techfreq for permission for any modifications or changes. 
See LICENSE.txt or http://creativecommons.org/licenses/by-nc-sa/4.0/ for full terms.  
Note: Monetized videos/blogs showcasing this mod are allowed along as with credit to TechFreq.

