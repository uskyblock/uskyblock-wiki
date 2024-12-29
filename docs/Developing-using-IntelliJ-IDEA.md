![uSkyblock-Revived](http://i.imgur.com/JbSV18m.png)

This is a step-by-step guide on how to get your environment setup to develop the uSkyBlock plugin using [IntelliJ IDEA](https://www.jetbrains.com/idea/download/).

# TL;DR
## Requirements
* Download and Install JDK (http://www.oracle.com/technetwork/java/javase/downloads/index.html)
* Download and Install GNU Gettext (https://mlocati.github.io/articles/gettext-iconv-windows.html)
* Download and Install Git (https://git-scm.com/downloads)

## IDE
* Download and Install IntelliJ IDEA Community Edition (https://www.jetbrains.com/idea/download/)

## Source Code
* Check out from Version Control > GitHub > https://github.com/rlf/uSkyBlock.git 

  **NOTE:** If you want to contribute, make your own fork, and clone that (instead of the `rlf`)
* Wait for all dependencies and plugins to download (be VERY patient!)

# Detailed Description
Only needed if the TL;DR section above didn't cut it.
## Requirements
### Download and install Java Development Kit (JDK)

Go to http://www.oracle.com/technetwork/java/javase/downloads/index.html and download and install the JDK (don't install Netbeans, it's just a slow, bloated IDE for Java, IDEA is better!).

### Download and install GNU Gettext

For windows users, go to https://mlocati.github.io/articles/gettext-iconv-windows.html and download the GNU Gettext installer of your choice (for other platforms, get it here: https://www.gnu.org/software/gettext/).

Install the program to a location, preferably one without spaces in the file-path (just makes your life easier).

In this example: `C:\Programs\GNUGettext`

Take note of the install-location!

## IDE
### Download and install IntelliJ IDEA

Go to https://www.jetbrains.com/idea/download/ and download and install the Community Edition (free) version of IntelliJ IDEA.

Make sure to enable the following tools during installation:
* Git
* GitHub
* Maven 

# Getting the uSkyBlock source-code
Open IntelliJ IDEA, and chose the `Checkout from Version Control` option on the start-screen (or get to it from the `File > New > Checkout existing`).

Punch in the URL: `https://github.com/rlf/uSkyBlock.git` and chose a sensible location for your local version of the project, and press Clone.

IDEA will now download the complete project to your local harddrive, and open it for you.
Just click next through most of the wizards you will encounter.

Make sure you point IDEA to the proper JDK (downloaded above).
Once opened, IDEA will download all dependencies for uSkyBlock - so be patient at this stage.