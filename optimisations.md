# Minecraft optimisations

Now L has her new Ryzen rig and A will be installing minecraft on their machine with a gpu, things are looking up - none of us are liable to be CPU or RAM limited if you are playing on the server.

L, hoever, was playing last night on some of relatviely medium settings was getting some FPS spikes and low FPS in general.
Minecraft can be a daunting application to configure, with probably over one hundred settings; some pretty fringe, some with huge quality impacts.

To get around this I've come up with some options to configure that are utter performance gluttons, but that don't really add that much to the game.

I've also had an impression that the shaders we are using could be supoptimal, so have been investigating some that look just as lovely, but are less CPU/GPU intensitve.

The new shaders I've been looking at are:


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


# Texture packs

The texture (sometimes called "resource" packs) we use are chosen because they generally match up between the mods (Extended Caves we're looking at you), and they're not total eyesores.

I have complete texture packs for 128x, 64x and 32x. With some older cards we might see some real improvements in the 32x packs, so will be giving them a try.

