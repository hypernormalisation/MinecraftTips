# Troubleshooting

I'll list any issues I've encountered here, and any possible fixes.

## Java (JDK) version compatibility

Vanilla Minecraft comes with all the Java infrastructure it needs to run, but many modpacks are built on older versions of the Java Development Kit (JDK).

If you get crashes when trying to launch any instance of modded Minecraft, check the logs for any mention of Java; if you see it, you're probably using an incompatible Java.

JDK 8 is usually a good one to try.

If after install you still get errors, check your launcher to see what version of Java it is trying to use and make sure it's using the new one you've installed.

Platform specific fixes are as follows, or you can manually go to:
[Java SE Development Kit 8 - Downloads](https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html)

and download the platform-dependent installer.

### Windows
Following link has .exes to install the version of the platform you need.
[Java SE - Downloads \| Oracle Technology Network | Oracle](https://www.oracle.com/java/technologies/javase-downloads.html)

### macOS
This relies on homebrew
```bash
brew tap AdoptOpenJDK/openjdk
brew cask install adoptopenjdk8
```
Up-to-date commands and available jdk versions on that tap are available at:
https://github.com/AdoptOpenJDK/homebrew-openjdk

### Arch
```bash
sudo pacman -S jre8-openjdk
```
More info at: https://wiki.archlinux.org/index.php/Java

### Debian/Ubuntu
Not able to directly test but maybe try this:
[How To Install Java 8 on Debian 10/9/8 via PPA - TecAdmin](https://tecadmin.net/install-java-8-on-debian/)
