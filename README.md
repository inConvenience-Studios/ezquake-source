# (in)Convenience Quake
This is a Quake client based on EZQuake. This is to be used on a few games made by us.

## Features

 * Modern graphics
 * [QuakeTV][qtv] support
 * Rich menus
 * Multiview support
 * Tons of features to serve latest pro-gaming needs
 * Built in server browser & MP3 player control
 * Recorded games browser
 * Customization of all possible graphics elements of the game including Heads Up Display
 * All sorts of scripting possibilities
 * Windows, Linux, MacOSX and FreeBSD platforms supported (SDL2).

Our client comes only with bare minimum of game media. If you want to
experience our Quake engine with modern graphics and other additional media including
custom configurations, maps, textures and more, try using the [nQuake][nQuake]-installer.

## Support

If you have found a bug, you can open a new pull request. If you found a security vunerability, read `SECURITY.md`

## Installation guide

To play Quakeworld you need the files *pak0.pak* and *pak1.pak* from the original Quake-game.

### Install our Quake engine to an existing Quake-installation
Paste the excecutable into the Quake directory.

A typical error message when installing our Quake client into a pre-existing directory is about *glide2x.dll* missing.
To get rid of this error, remove the file *opengl32.dll* from your Quake directory.

### Upgrade an nQuake-installation
If you have a version of [nQuake][nQuake] already installed you can upgrade our Quake client by extracting the new executable into the nQuake-directory.

### Minimal clean installation
If you want to make a clean installation of our Quake engine you can do this by following these steps:

1. Create a new directory
2. Extract the ezQuake-executable into this directory
3. Create a subdirectory called *id1*
4. Copy *pak0.pak* and *pak1.pak* into this subdirectory

## Compiling

### Compiling a Windows binary

#### Using Ubuntu Bash (WSL)

You can use the new Ubuntu Bash feature in Windows 10 to compile our Quake client for Windows.

To enable Bash for Windows, press the `Start` button and type `Turn Windows f` and select `Turn Windows features on or off`. Scroll down to `Windows Subsystem for Linux (Beta)` and enable it.

Now press WINDOWS+I, go to `Update & security` and then to the `For developers` tab. Enable `Developer mode`.

Now press the `Start` button again and enter `bash`. Click it and install Bash.

Enter the following command to install all required prerequisites to build our Quake client:

```
sudo apt-get install -y git mingw-w64 build-essential libspeexdsp-dev dos2unix pkg-config
```

Now clone the source code of our Quake client:

```
git clone https://github.com/inConvenience-Studios/inconvenience-quake storquake
```

Make sure line endings are not CRLF:

```
dos2unix *.sh
```

Now build the executable:

```
EZ_CONFIG_FILE=.config_windows make
```

Copy the compiled binary to your Quake folder, the binary is called `ezquake.exe`.

##### Tree

Id Tech 2 (Quake 1)
      |
A few source ports
      |
EZQuake
      |
storquake
