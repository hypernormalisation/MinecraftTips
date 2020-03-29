# Coronacraft

A document detailing wonderful world of Minecraft in March 2020, to help us choose the most fun MC setup for our quarantine time.

Troubleshooting can be found at [this page](https://github.com/hypernormalisation/MinecraftTips/blob/master/troubleshooting.md).

## Why Minecraft?

- low barrier to entry in cost/device performance
- drop in/drop out gameplay
- no gamer rage so Steve/Scott/Gavin don't smash peripherals
- trains - lots and lots of trains. Seriously Ayn Rand would love this game.

But moreso, I will also advocate that we play a modded version of Minecraft.
Don't worry if you've not done it before, it's incredibly easy today!

## Why modded Minecraft?

Obviously we need accounts for the Java version of MC.
We all seem to already have those, and if you want to play vanilla you just use the vanilla launcher and a vanilla server, like the other night on Roddy's server.

But vanilla is just the tip of the Minecraft iceberg.
Mods and mod packs are the life-blood of the game; personally speaking I've found good mod packs to be considerably more fun than vanilla, especially on small-to-medium sized co-op servers with friends. It's cool to show off the different things you're building!

e.g. I focus on building industrial stuff from tech mods, meanwhile Lauren is exploring caves for rare materials, meanwhile Will has built a wizard's tower and is creating powerful magics.
I can provide Will with mass materials to build his tower and fuel his dark machines, and he in turn can provide Lauren with powerful spells and equipment to go spelunking, who finds us rare stuff to build even more powerful or cool machines.

Can get real satisfying. Ultimately, the extra variety that the mods provide really enhance the "look at this cool thing I made!" response of the game, which is the most fun part about MC.

There are also some really nice quality-of-life features like minimaps and inventory improvements that can make mods much more accessible than Vanilla.

---
# Client-side launchers

If you want to play the vanilla minecraft, you download the installer and run the client. Simple.
If you want to install mods manually it's possible but can be a total pain.

So, many communities have sprung up with their own tools, usually called *launchers*,  to manage modding (and sometimes more) for you.

### What launchers do for you and considerations

#### The good
A good launcher will:
- be able to download any version of the vanilla MC game you want (important as some mod packs run on different versions)
- provide a large section of mod packs to browse from, so you can shop around and easily install them in their own isolated instances
- provide additional settings to more finely control your Minecraft performance - e.g. by letting it run with more reserved RAM (rather than using arguments in the Java executable, the way it's done in vanilla)
- some launchers also provide easy ways to install new texture packs

#### The bad

Mod packs, especially larger ones, can substantially add to the initial load time of the game (although most are well enough optimised that in-game performance is not very affected).

To ensure we can all play the mod pack we settle on without huge wait times, I'll perform some testing on how long it takes from clicking "play" on the launcher button to getting to the MC in-game menu, the biggest time-sink.

Mod packs are run once to the welcome screen to allow any necessary assset construction, quit out, and the second one is timed, to be more representative of the average boot time for the client.

All the following test times were performed on a i7-6700k @ 4.0GHz, with 16GB of RAM. That processor is a quad-core, hyper-threaded model so to estimate your own times scale by your own CPU capbility (the CPU usage time is not always at 100% when the mods are initialising so a comparison calculation with a less powerful CPU is a worst-case scenario and if, like Karl, you own Deep Blue you are probably fine).

---
# Launcher comparisons

So let's take a look at some of the launchers out there and see what they offer, and what mod packs feature on them.

I have also checked compatibility with Windows/macOS/Linux - but even if something doesn't work on one of the three (probably Linux) there are two possible fixes:
- the mod pack is available on another launcher which does work on Linux
- manual installs (possible but would like to avoid)

---
## Twitch (formerly Curse)

The Twitch application has a powerful tool built-in for automating minecraft for you.
From the application home page click "Mods" and you'll see a variety of supported games that Twitch can manage for you including Minecraft(note to Lauren: Darkest Dungeon is here too!). That menu takes you to the mod browsing and launching screen.

### Installs/compatibility

#### Windows &#x2611;
installer available [here](https://www.twitch.tv/downloads)

#### macOS &#x2611;
```bash
brew tap AdoptOpenJDK/openjdk && brew cask install twitch
```
#### Arch &#x2612;
Lutris installs Twitch app successfully but the Mod tab does load - I suspect this is an issue with 32-bit libraries, and am not sure how to solve. Manual installation of any mod is still hypothetically possible

### Mod packs and performances

Mod pack              | Startup Time | Peak Memory Usage (GB) | Notes
 -------------         |:-------------| :-- | :--
 RL Craft | 0:54 | 6.5 | Relatively new, hard as nails realism pack. You will die and die lots, but I have watched some streamers play it and it looks actually very good fun.
Sky Factory 4 | 2:38 | 7.5 | "Sky block" type of game, but one that allows you to simulate all kinds of survival situations (e.g crash spaceship landing, worlds made of floating islands etc)
Roguelike Adventures | 2:04 | 8 | Quest-oriented modpack.
SevTech Ages | N/A | 9.1 | Crashed. Cool concept though, progression through the ages. Would be nice to get working.

---
## Feed the Beast (FTB)

One of the biggest modpack production teams, they have migrated from Twitch to their own launcher.
Their releases, while sometimes available elsewhere, are more recent and stable on their own launcher.
Have personally played several of their releases and had great fun!

### Installs/compatibility

All platforms are compatible and tested by me :)

A general tip is to go into the application settings and spare as much RAM as you can for the game - 4-6GB seems to help things run very smoothly.

#### Windows/Debian &#x2611;
Installers available [here](https://www.feed-the-beast.com/)

#### macOS &#x2611;
Had difficulties with Java install via homebrew so install Java 8 from [here](https://www.java.com/en/download/mac_download.jsp)

Then run a:
```bash
brew cask install feed-the-beast
```
#### Arch &#x2611;
Package `feedthebeast` available on AUR, e.g. 
```bash
yay -S feedthebeast
```
or the equivalent for your AUR helper

## Mod packs and performances

 Mod pack              | Startup Time | Peak Mem Usage (GB) | Notes
 -------------         |:-------------| :-- | :--
FTB Academy | 1:01 | 7.1 | Tutorial for FTB-style modpacks and questing, plus all the usual stuff to do once you do the tutorial.
FTB Continuum | 1:33 | 7.3 | Kitchen sink pack, loads to do, can go to space, plus quests to help newer players get used to the mods.
FTB Infinity Lite 1.0 | 1:27 | 7.1 | Older version of MC, aims at being lighter but is not lightweight enough imo to justify going to an older MC version
FTB Ultimate Reloaded | 1:45 | 8.0 | A revision of an old classic FTB pack from 5 years ago (that I played and enjoyed), but with a slew of optimisations on the server and client side.
FTB Revalation | 3:48 | 10.1 | Absolutely every mod you could possibly want, but the massive startup time makes it undesirable for us to run.

---
## Technic Launcher

This is a launcher based around fun, sciency mod packs.

Just a very brief note to say I could not get the Technic Launcher working on the two platforms I tried, encountering 2 separate errors.

So this one is a no-go.

---
# Conclusions

If we do want to play a modded server, I would advocate for one of the Feed the Beast mod packs, for the following reasons:

- the mod packs are full of high-quality mods
- I was able to get mod packs working on Windows, macOS, and Arch Linux using the FTB launcher
- the startup times are acceptably low (in the realm of minecraft modding anyway)
- the performance in-game is solid, given the FTB team have been working for more than a decade to make their packs perform more smoothly.

If people agree and are interested, the next step is setting up a server!
