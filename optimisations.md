# Minecraft optimisations

Now L has her new Ryzen rig and A will be installing minecraft on their machine with a gpu, things are looking up - none of us are liable to be CPU or RAM limited if you are playing on the server.

L, hoever, was playing last night on some of relatively medium settings was getting some FPS spikes and low FPS in general.
Minecraft can be a daunting application to configure, with probably over one hundred settings; some pretty fringe, some with huge quality impacts.

To get around this I've come up with some options to configure that are utter performance gluttons, but that don't really add that much to the game.

I've also had an impression that the shaders we are using could be supoptimal, so have been investigating some that look just as lovely, but are less CPU/GPU intensitve.

So who is this article for?
- anyone wanting to try out new shader packs to see how things look and feel (recommanded)
- or if your game isn't consistently hitting 50-60fps.

# Some testing notes

I have a reasonably powerful machine, so it's hard to properly test how certain configurations will run on certain hardware.
To mitigate this a little, I'm using the application MSI Afterburner application to track my GPU usage, as well as memory consumption.

Now, this is obviously not a perfect map - some GPUs are better at some things than others, especially between hardware generations.
But should give a decent idea of how a modern GPU handles minecraft with shaders and good resource packs running.

But of course *just because a setting has minimal performance for your my does not mean that will hold true for your card*!

In each test I will run around a single player world for a while and not the max GPU and RAM usages.

I will do so for a permutation of:
- in game settings
- texture pack size
- shader pack

# Some key video settings
All these checks are run with me running SEUS shaders, 128x texture packs, on 1080p.

## Top-level settings settings.
For all these changes my GPU/VRAM usage didn't change all that much - instead I checked framerate concistency.
These are only the settings that affect performance.

- graphics (fast/fancy): 5-20 frmea benefit depending on location, no visible difference to me/
- smooth lighting: having this set to 50% and maximum is probs worth the couple of dropped frames
- dyanamic lights: have these set to fast - they let your torghes light the ambient area, and the maximum option is a frame killer with very little noticeable difference.
- Use VBOs: a best as I can tall, have it on. Possible gains.
- render distance: it's important to remember that multiplayer servers only send clients chunk info at MAX away, despire what you have in your settings. There can, however, be use in running a slightly higher one, say 22-24 or so - this persists where you might have just visited in the world if you're on the move and can look good. Otherwise - this setting will murder even a top-level machine if you set it much above 32.

## Animations

You generally want all of these on for the look and feel of the game.
If you're having FPS issues setting particles to "decreased" or "minimal" may be of use.


## Details
- clouds: keep them off, the texture pack supplies their own, better looking ones
- trees (fast/smart/fancy): probably worth keeping this set to "smart" so the trees are a little transulcent. If you're having frame issues then they still look fine in "fast".
- fog: very little difference for me, but my testing was in a sunny biome. Could have significant effects in storms etc.
- translucent blocks: very little difference
- swamp colours: keep on for looks
- alternate blocks: same as above - can look dodgy without

None of the rest of the Details video options seem to matter very much.


## Quality
- mipmap settings don't do much for me but someone confirming this would be nice
- the anisotropic filtering/antialiasing are not enabled when shaders are so you can skip this
- emissive textures you *very much want on* as they make some shader packs look very wonky
- better grass and snow can maybe save a couple of frames, but not much. If you're struggling turn them off.

Nothing else in the Quality options seems very relevant to performance.

## Performance
Most options here can be left apart from the following:

- Smooth FPS: seems to cost wayyyyy too many frames in its pusrsuit of steadying the output, turn it off.
- Chunk Updates: put it lower if you have lag or FPS issues, otherwise 4-5 seems more responsive.


# Shader packs

The two shader packs being used to far are SEUS and Sldur's (high/medium/lite)/

SEUS is temperamental with regards to GFX card drives (but looks lovely if it runs). Sildurs also looks great but both ot eh above tend to be significant resource drains

Now of course some shader packs, like Sildurs, are *wildy* configurable - so if you're getting poor performance using Sildur's then you can play around with the settings.

I might write about that at some point, but in the meantime I looked into some comparisons of shader packs running on my machine. Some more are tested herein.

# Texture packs

The texture (sometimes called "resource" packs) we use are chosen because they generally match up between the mods (Extended Caves we're looking at you), and they're not total eyesores.

I have complete texture packs for 128x, 64x and 32x. With some older cards we might see some real improvements in the 32x packs, so will be giving them a try.


To push my machine a bit, I'm running max settings and 128x texture packs, but imposing a 60fps limit so the results are more transferable to older machines.

# Test results
For most cases, the texture packs used do not influence the GPU usage, just the VRAM.

## SEUS-RENEWED

GPU ave 60%

128x - 3 GB VRAM

64x - 2.4 GB VRAM 

32x - 2.2 GB VRAM

Only powerful machines (with the right drivers) can use this configuration.


## Chocapic
Now let's look at something new with the Chocapic v7 shaders I've been running.
They are similar to SEUS but with a lightly more photorealistic aesthetic.

They also come in a variety of shader packs:
- toaster
- lite
- low
- medium
- high
- ultra
- extreme

So with the aim of looking at how lower-end machines can perform with nice shaders, let's test a bit.

- Lite: 14% GPU usage, 1GB VRAM @ 64x textures - very smooth but no reflections
- Medium: 20% GPU usage, comparable VRAM
- High: 38% GPU usage
- treme @ 218x textures: 65% with 2.4 GB VRAM.

## Sildurs

Out of interest, let's look at how Sildur's stack up here, given they have already been used by players on the servers:

- Sildur's lite: 35%, 1.9GB VRAM
- Sildur's medium: 38%, 1.9GB VRAM

Sildur's looks very much like the Chocapic ones, but appear quite a bit more resource intensive.

I alse notice that Sildur's does strange things with shadows of smaller objects like grass, that I didn't observe in the other shader packs.

## Conclusion

If you're running a high-end machine that deals with SEUS's shaders well, stay the course

If you are either:
- runnng a high-end machine with SEUS graphics drivers issues
- running a lower-end machine

...then you should check out the updated version on the repo called "Liquid_foorball_Craft".
It's too big for github so you can find it on my Drive:
https://drive.google.com/file/d/1Yq5Ox5UqxdsdP1-GCFSSYYwZ5jaE8e7f/view?usp=sharing

If comes configured out-of-the-box to use the Chocapic medium shaders, and the 32x versions of the Sphax texure packs. Using those should give users of less powerful PCs a bit more performance and still look very much like what they're used to with Sildur's.

Of course, the container comes with the full new expanded set of shaders, and the 128x/64x/32x versions of the texture packs - so you can mix and match to your heart's content, find the right looks-to-performance ratio for yourselves.

If you want to transfer your map to the new instance rather than alter your existing client, you can just copy over your XartoWorldMap folder to the new instance.

## Known Issues

- There is still a problem with Xaero's minimap when trying to create waypoints under certain conditions - this can break your container in ways we don't yet understand so avoid waypoints for now
- When many people are on the server, we notice slowdown in certain areas like minecarts. We'll be considering how to reduce server lag without having to upgrade the server machinery very kindly offered by Will.





