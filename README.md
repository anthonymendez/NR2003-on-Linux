# NASCAR Racing 2003 Season Linux Installation Guide

## Contributor Note

If something doesn't work you had to do something slighty different, feel free to make a pull request for any suggested edits.

## Requirements

* [Wine](https://wiki.winehq.org/Download)
* [Lutris](https://lutris.net/downloads)
* NR2003 Installation Files
* NR2003 1.2.0.1 Patch Installation Files
* NR2003 1.2.0.1 No-CD Crack File

The NR2003 files I will let you learn how to aquire yourself ;)

## Steps to Install and Patch

1. Lauch Lutris and select `Add games to Lutris` (the + on the top left).

1. Select `Install a Windows game from media`.

1. Type in `NASCAR Racing 2003 Season`.

1. Click the `Install` button where it says `Setup file`.

1. Select a directory to install your game. I have the path `Games/NR2003` under my user directory. `/home/anthonym/Games/NR2003`.

1. Click `Install`.

1. Click `Browse...` and find your installation files. Select `Setup.exe` and click `Continue`. 

The "wine configuration is being updated" should come up after. Then the NR2003 installation process should begin. You should hear the test audio file and will be prompted. Go through the installation process as normal, clicking all the defaults. 

**Important Note**: The setup window may glitch out or be blacked out. Program is still working, you just have to click and drag the window to get it to appear normally again.

8. After the installation procedure is done, create a folder in the game directory, under `drive_c`. Copy your 1.2.0.1 installation files there. In my case, I placed them in `/home/anthonym/Games/NR2003/drive_c/PatchFiles`.

1. Go to Lutris, select `NASCAR Racing 2003 Season` from your games library. Next to the wine logo at the bottom, click the up arrow, and select `Run EXE inside Wine prefix`. 

1. Select the 1.2.0.1 patch exe file you placed in the game directory.

1. Go through the installation procedure.

1. Afterwards, you can copy your No-CD EXE file into the directory.

1. One last step. In Lutris, right click `NASCAR Racing 2003 Season`, click `Configure`.

1. Go to `Game options` and click `Browse...` for `Executable`. Select `NR2003.exe`. I noticed that it would open up the `Sierra.exe` instead of the game exe.

1. Now you can launch the game through Lutris and it should work. The Graphics Configurator will launch and you can put in your resolution and settings you prefer. I've tried DirectX and OpenGL with no issues. If you would like to re-open the graphics configurator again to change your settings, you can do the same thing we did with installing the patch file. `Run EXE inside Wine prefix`, then select `config.exe`.

And there you go! You should have NR2003 working on Linux! 

## Wheel Support

My Logitech Driving Force GT steering and throttle worked, but not the brake pedal. I used [pyLinuxWheel](https://gitlab.com/OdinTdh/pyLinuxWheel) to get it to work and adjust settings. There is also [Oversteer](https://gitlab.com/OdinTdh/pyLinuxWheel) but I have not tried it out for myself. Any changes in pyLinuxWheel should propagate live to the game with no issue.

## Bugs

### Audio Glitching

You may have some audio glitching when on track. I fixed this by disabling 3D Audio in the in-game Audio menu.

### 60 FPS Locked on Windowed Mode

Unfortunately, haven't found a fix to get around this.
