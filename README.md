# ProjectBT
An MKWii Battle improvement mod. Adds new features, changes, and fixes to Mario Kart Wii's Battle mode. There are many mods out there for VS but very few that develop the battle mode of the game, and most players play VS mode over battle leaving a very small community of battlers left. This mod aims to improve battle mode to attract more players and create a bigger and better community. This adds many features that long-time battlers have long been wanting.

This repository is a re-write of an older, outdated version of the project: https://github.com/Namelesss1/Mkwii-Battle-Mod

## New Features

- **Two new battle gamemodes** alongside Balloon Battle & Coin Runners
  - _Shine Thief:_ Very similar to Shine Thief from Mario Kart 8 Deluxe. Everyone battles for the Shine Sprite (which is actually a single coin). To win, a player must hold on to the shine for at least 30 seconds. Points are based on how many seconds a player has held on to the shine for (e.g. 10 seconds held = 10 points). When losing the shine and picking it up again, the timer for players will pick up where it last left off. If a player loses the shine with under 10 seconds left, they will need to count down from 10 seconds again the next time they pick it up.
    
  - _Elimination:_ A battle-royale style gamemode where players are eliminated. There is a grace period where players will collect as many points as they can. Once the grace period is over, every 15 seconds the least-scoring players will be eliminated until there is only one (or no) players left standing. Placement is based on order of ellimination.

- **Free-For-All (FFA) mode:** Battle without teams! You can hit and score off of whoever you want, its everyone for themselves. How well you place depends only on how well you do individually.

- **Custom Battle Tracks**: Instead of just 10 battle stages, you can choose from among 37 different battle stages including the original battle stages, custom tracks, and retro tracks.

- **All or Nothing mode**: This optional way of playing battles is very intense. You can win it all, or lose it all. A rewarding yet punishing battle option which behaves differently for each gamemode:
  - _In Balloon Battle:_ You can +5 points for popping someone's last balloon. But you lose ALL points when you lose your own last balloon.
  - _In Coin Runners:_ Players drop ALL coins when hit in any way, no matter how many coins they had. If a player is hit with a shroom or a star, all of their coins will be stolen and given to the other player!
  - _In Shine Thief:_ When you lose the shine, your time left with shine will be reset back to the full 30 seconds. This means that to gaurentee a win, a player must hold the shine for 30 seconds straight without losing it.
  - _Elimination:_ Same as in Coin Runners, and there is no grace period. Players will begin to be eliminated right after the first 20 seconds

- **New Items**
  - _Booper_: A mix of a boo and a blooper ("Boo-per). Does the same thing as a blooper, but also steals things from the highest-scoring player like an automatic-mushroom. In balloon battle, it steals a balloon from highest-scorer and you gain a point. In Coin Runners & Elimination, it steals coins from highest-scorer and gives them to you. In Shine Thief, it steals the shine from whoever currently holds the shine.
  - _Triple Bombs_: 3 bob-ombs that rotate around you. Replaces shocks
  - _Triple Fibs_: 3 fibs that rotate around you. Replaces Bullet Bill

- **New Item Settings**: Similar to the strategic/aggressive settings that already exist offline. You can select what kind of items will appear in online frooms and offline play.
  - _Bob-omb Blast_: Bombs only. Players can stock up on up to 5 or 6 bombs and use them whenever they please. When hit by a bomb, players keep their items and spin out as if hit by a banana peel.
  - _Aggressive Items_: More chaos an action in battles. Power items are more likely to occur which include items like megas, stars, triple bombs, reds, booper, etc.
  - _Snipemode_: A true show-case of item skills, strategy, and how well players aim. Only strategic items appear (bananas, fibs, greens, mushrooms, rare bombs, and triple variations of these items)

- **Ability to use all Vehicles in Battle**: Usually battles only allow Standard karts/bikes. However, this option allows you to use any vehicle you want from VS as well. From Flame Runner to Cheep Charger, you can choose them all.

- **"Predicible Teams" online froom option:** Normally, battle teams in froom are decided randomly (regardless of BR or join-order) but this option allows froom hosts to have teams based on join-order. The first half of the room to join will be on red team, the second half will be on blue team. This is done by player slot id. Useful option for any organized events where you want to gaurentee certain players on the same team (e.g. battle clan wars or tournaments)
  
- **Ability to change characters and vehicles between battles**

## Changes, balance, and tweaks

- **Balloon Battle**:
  - Start with 5 balloons instead of 3.
  - Respawn back with 4 balloons instead of 3.

- **Coin Runners**:
  - Regardless of the amount of players, the same amount of coins will always spawn. This means you can still have 50+ coins even in an online 1v1.
  - The minial coin loss has increased from 3 to 4.
  - Players steal 5 coins instead of 3 when using shrooms or stars
  - Players lose 40% of coins when hit in general instead of 50%.

- **Items**:
  - Item probabilities now take into account how well a player's team is now doing. If their team is winning, they will be less likely to get power items (though still possible) to prevent a common occurrence where the winning team continues to get many power items despite the fact that they are winning, making it very difficult for the losing team to make a comeback.
  - Item probabilities have been tweaked
  - Bullet Bills replaced with triple fibs (since they were unused in battles)
  - Shocks replaced with triple bombs (since shocks were underpowered)
  - Bloopers replaced with new Boo-per (original blooper was underwhelming in battles)
  - Banana limit increased to 19
  - Fib limit increased to 12
  - Bomb limit increased to 18 (bob-omb blast)
  - Green limit increased to 14
  - Red limit increased to 10
  - Blue shells are now draggable

- **Track Changes**:
  - Delfino Pier now has six extra item boxes: A pair of item boxes on the east end of the map, and four more in the corners of the upper level.
  - Chain Chomp Wheel star boxes replaced with regular item boxes
  - Thwomp Desert Item Boxes are now distributed around the map, instead of them all being jumbled around the center.

- **WorldWide Changes (region 700)**
  - WW battle rounds cycle from Balloon Battle -> Coin Runners -> Shine Thief -> Elimination, then repeat. With the following exception: Shine Thief and Elimination will require at least 3 players. Otherwise, shine thief becomes balloon battle and elimination becomes coin runners.
  - Rooms with an even number of players will be teams, and odd will be in FFA mode. With the following exception: Shine Thief and Elimination will always be FFA regardless of player count.
  - Starting BR limit will be 7000 instead of 5000
  - Lowest BR limit will be 6500 instead of 1
  - How many points a player scored in a battle will be added to final BR calculation. So the more you score, the more BR you can gain. In balloon battle, your exact score is added on to what you earn/lose. In Coin Runners, your score divided by 2 is added. In shine thief, score divided by 3 is added. In elimination, score divided by 4 is added. For example, if you scored 5 points in balloon battle, and you're set to gain +27 BR, you will earn 27 + 5 = 32 BR. If you scored 20 coins in Coin Runners, and you're supposed to lose -12 BR, then you have 20/2 = 10, then -12 + 10 = -2. So a -2 BR loss instead of -12.
  - Players on winning team cannot lose BR. So if normally you would lose -20, you will get +0 instead if your team won.

- **Menu Changes**
  - The offline Grand Prix/Time Trials/VS/Battle screen has been replaced with a battle select screen. Grand Prix leads to elimination. Time Trials leads to Shine Thief. VS leads to Balloon Battle. Battle leads to Coin Runners
  - Offline multiplayer VS/Battle select screen replaced. Doesn't matter which button is chosen
  - The balloon battle/coin runners select screen is now an FFA/team select screen
  - Battle settings screen offline has some buttons replaced to add optional toggles for the new features like all vehicles, all or nothing mode, item settings, etc.
  - VS settings screen in multiplayer offline has some buttons replaced to add the same optional toggles, as well as battle gamemode select.
  - When starting a froom, the options have been changed: VS has been changed to elimination. Team VS has been changed to Shine Thief.
  - Some froom messages are now used to load custom settings (All or Nothing, All Vehicles, FFA, etc.). These can be toggled only by the froom host.

- **Other**
  - Instantly Respawn back on the map when falling off. Quicker respawn in balloon battle after losing all balloons.

## List of Tracks and cups (Subject to change) - 37 tracks total
- _Wii Cup_: Block Plaza, Delfino Pier, Funky Stadium, Chain Chomp Wheel, Thwomp Desert (All by Nintendo)
- _Retro Cup_: Leads to all retro tracks and custom tracks below
- _Balloon Cup_: SMG Ghostly Arena Plent (King Boo Gaming), Cistern Channel Garden (Bri911 & SUPERsaiyanPaco), Mushroom Canyon (KantoEpic & Yoshivert99), Spade's Battle Course (Spade)
- _Coin Cup_: Traverse Town, Switch Battle Stadium, DKR Icicle Pyramid, DKR Smokey Castle
- _Shine Cup_: Space Battle 5, BAR! Castle, BAR! Parkade, Lava Battle
- _DS Cup_: 3DS Sherbet Rink, 3DS Wuhu Town Nighttime, DS Twilight House, DS Palm Shore
- _GCN Cup_: GCN Block City, GCN Cookie Land, GCN Pipe Plaza, GCN Luigi's Mansion
- _N64 Cup_: N64 Block Fort, N64 Skyscraper, N64 Big Donut, N64 Double Deck
- _GBA Cup_: GBA Battle Course 1, GBA Battle Course 2, GBA Battle Course 3, GBA Battle Course 4
- _SNES Cup_: SNES Battle Course 1, SNES Battle Course 2, SNES Battle Course 3, SNES Battle Course 4

## Planned Features/Changes
Features that do not exist in the project yet, but may in the future (If possible)

- Support for PAL and NTSC-J
- Megas, goldens, and star timers will be reduced by a second
- Snipe Rewards: Landing a snipe with a banana or fib directly on a player will be extra-rewarding. In balloon battle, you earn +2 instead of +1. In Coin Runners, Shine Thief, and Elimination, those dropped coin will be transferred directly to you (as if you shroomed them).
- Elimination will be a mix of balloon battle and coin runners instead of just coin runners-based.
- The bigger the room, the more players are eliminated at once in Elimination
- Add the timer graphic to local multiplayer
- Add proper randomization/in-order track logic to track selection both offline, and when voting "random" online.
- Have offline custom settings save for the next time you boot the game (like regular existing settings do)
- Have multiple highlighted backgrounds in offline custom settings menu so players can see exactly which settings are active
- Add team colors to every vehicle when teams are enabled (e.g. Red-team cheep charger) 
- Any more thought of/suggested

## Important notes

- Currently, this project is only available in NTSC-U.
- More updates to this project to come, but very slowly possibly due to time restrictions.
- The host must wait until everyone is in the froom to choose custom settings. Otherwise the settings will only apply to the players that were already in the room.

## Known Bugs

- Online voting timer hangs when it ends while on screen 0x6e/0x6f (VS cup and VS stage select), no automatic menu presses
- Online voting cannot go back to battle cup select once you choose VS cup select
- (Possibly) blue shells will target the wrong player in FFA mode, due to them still following team-restrictions only targetting someone on the other "team"
- Visual coins on screen when playing CTs stack weirdly
- In bob-omb blast when teams are active, the score update graphics (+1 -1) don't appear after scoring points
- Local multiplayer crashes randomly at times after leaving a battle/battle end
- In local multiplayer, some tracks (e.g. Space Battle 5) causes messed up scores in Shine Thief (and possibly elimination)
- In local multiplayer, bob-omb counter positioning is off, possibly being placed right where team score counter is
- In FFA online, the screen that shows everyone's course votes still shows team colors.
- Not a "bug" since this is a feature of the original game, but the timer graphic does not appear in local multiplayer which is disadvantageous in elimination & shine thief.
- The only tracks that can be picked by selecting "random" in online voting are the orginal 10 battle track slots.
- Picking "random" or "in-order" battle tracks offline only choose from the original 10 battle track slots.
- Custom froom settings won't apply if someone is spamming messages over and over again
- Guests are not properly accounted-for in predictable teams froom setting

## Credits
Anyone that has contibuted to this project in some way

# Code Credits
Credit for people that have directly helped or made codes that were used or helpful in development of this project.

- MrBean35000vr: Change Vehicles Between Races code, ct-code engine, many memory addresses used to prevent crashes and such with screen loading
- Chadderz: ct-code engine
- Davidevgen: Item limiters, instant respawn
- Seeky, TheLordScruffy: mkw-structures documentation (https://github.com/SeekyCt/mkw-structures/blob/master/itembehaviour.h)
- SkullFace, CLF78: Item Damage Type modifiers
- CLF78: Disable Item Poof
- Bully: Always Have Item
- Ro: Start with X balloons, let me know about balloon positioning fix
- Dea: Balloon Positioning fix
- Joshua MK: Custom Laps Mini
- Vega: Stacked Teams (Addresses used for predictable teams feature), amazing PowerPC tips and tutorials 
- salmon01: Float to integer conversion
- _tZ: Unlock everything without save
- More possible. Apoligies if I missed someone, please let me know and will gladly add to the list.

# Testers
People who have helped me test and play this project since the beginning (2019) and before its public release (2023). 

- Isa9998
- Becca/Scarlet
- Kev
- Yousef9998
- Kebab
- Diamond
- Teovani69
- Spade
- Chenz
- Karma
- Tony
- MaxMK

# Special Thanks
People who've contributed to many ideas, support, have helped play and test it a lot.

## Code Usage
Feel free to use any of the code here for your own projects or codes. Just give me some credit, I would appreciate it for the work gone into it so far.

## Contributing, help, suggestions, and feedback
Help is appreciated! :) Anyone is welcome to let me know what they think about the features and changes, whether the game is balanced enough, what new things should be added, etc. Please let me know of any more bugs found that are not already on the known bug list. Further, anyone is welcome to help out on the code-end of things if you see any way to fix some bugs, clean up some unoptimized code (there is plenty of that), or add any new features that are listed on the Planned Features section.

## Building The Project from the source code
See building.md
