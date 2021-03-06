# Coronacraft - a lightweight Minecraft container

We have configured a server using a lightweight set of mods, based upon generating interesting world and some quality-of-life improvements.

I've created a *containerised* version of Minecraft that includes all of those mods, plus texture packs for the basic Minecraft game, and all the mods, plus fancy shaders for lighting and water effects.

If you want to play, these are the instructions. But you will need a Mojang account that owns the *Java edition* of Minecraft to do so.

In brief, we will download an open-source program called multiMC (if you know coding, think "Docker for Minecraft"), and then download an image from this repository to use with multiMC.

Then contact me in private or a group chat to get the server details!

## multiMC application

multiMC is downloadable here: https://multimc.org/#Download

It's cross-platform so works on Windows/macOS/Linux.

#### JDK
You may need the Java Development Kit v8 also installed to use it (or build it on a non-Debian Linux distro).

All the installers for your OS can be found here:
https://www.oracle.com/java/technologies/javase-jdk8-downloads.html

## Download Coronacraft.

In this repository there are some .zip files in the containers folder.

Each of these can be imported to multiMC to configure your client, complete with shaders and mod packs.

There are 3 versions available, given in the table below, with different graphical presets, texture qualities, and shaders enabled.

For frames per second (FPS) references, my machine is a i7-6700k 4c/8t processor with 16GB of RAM and a GTX1070 dedicated GPU. So, very good but still about 5 years old.

It's also important to note that all of these can be downloaded and configured independently! So you can try out all 3 at once and find the best one for you, and then of course tweak the in-game options to make things look better or run smoother.

Version   |  Notes | FPS on my machine
 ------------- |:-------------| :-----
Coronacraft_1.0.zip | Meant for powerful machines with a good dedicated GPU. If you have a recent gaming PC, this is for you! Uses 128x128 textures and includes SEUS and Sildur's High shaders. Sildur's is default because SEUS is temperamental, but can look great if it works for you. | 60-80
Coronacraft_lite_1.0.zip | If your machine has a reasonable, but not amazing, dedicated GPU then this is a safe bet. Uses 64x64 textures and Sildur's medium shaders. Slightly lower graphics settings to save frames | 80-100
Coronacraft_potato_1.0.zip | If your machine has no dedicated GPU or a really bad one, this might do the trick in a pinch. Uses 64x64 textures and Sildur's lite shaders. | 130-180

If potato is still too much for your machine, you can revert to the default Optifine shaders in the options, or just turn them off to save some frames.

Links here:

https://github.com/hypernormalisation/MinecraftTips/blob/master/containers/Coronacraft_1.0.zip

https://github.com/hypernormalisation/MinecraftTips/blob/master/containers/Coronacraft_lite_1.0.zip

https://github.com/hypernormalisation/MinecraftTips/blob/master/containers/Coronacraft_potato_1.0.zip

## Install

Once you have multiMC opened up, you can untick the google analytics reporting, and find yourself in the main menu.

![](img/1.png)

At the top right of the screen, open the account manager and add your Mojang account email/password.

![](img/2.png)

Enter your details here

![](img/2_5.png)

Your account will now be added

![](img/3.png)

Then click "Add Instance" in the top left, and click "Import from zip".
Give the location of the Coronacraft zip file you want to add
![](img/5.png)

![](img/6.png)

Then simply double click the icon of your newly-added Coronacraft instance, and it will boot to the client after downloading some libraries.

![](img/7.png)

Double click on that, or hit "launch" on the right panel annnnd

![](img/8.png)

hopefully you end up here!

No need to configure shaders or texture packs, just go straight to the server or test your graphics settings on a single player game!

(If you play single player, set the world type in the creation to "biomes o plenty" to get the cool stuff also generated.)
