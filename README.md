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
# Twitch (formerly Curse)

The Twitch application has a powerful tool built-in for automating minecraft for you.
From the application home page click "Mods" and you'll see a variety of supported games that Twitch can manage for you including Minecraft(note to Lauren: Darkest Dungeon is here too!). That menu takes you to the mod browsing and launching screen.

### Compatibility
- Windows &#x2611; 
- macOS &#x2611; 
- Arch &#x2612; - Lutris installs Twitch app successfully but the Mod tab does load - I suspect this is an issue with 32-bit libraries, and am not sure how to solve. Manual installation of any mod is still however possible

### Mod packs and performances

Mod pack              | Startup Time | Peak Memory Usage (GB) | Notes
 -------------         |:-------------| :-- | :--
 RL Craft | 0:54 | 6.5 | Relatively new, hard as nails realism pack. You will die and die lots, but I've watched some streamers play it and it looks actually very good fun.

Sky Factory 4 | 2:38 | 7.5 | "Sky block" type of game, but one that allows you to simulate all kinds of survival situations (e.g crash spaceship landing, worlds made of floating islands etc)

Roguelike Adventures | 2:04 | 8 | Quest-oriented modpack.

SevTech Ages | N/A | 9.1 | Crashed. Cool concept though, progression through the ages. Would be nice to get working.
