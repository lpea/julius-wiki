Julius supports Windows Vista and higher. Windows XP has limited support.

1. Install Caesar 3 using the provided installer (GOG/Steam/CD-ROM). When installing from CD-ROM, please select the "Full installation" option, otherwise you'll experience missing sound and videos.
2. Download the [latest release](Julius-release) of Julius or compile from source.
3. Copy julius.exe, SDL2.dll, SDL2_mixer.dll and libmpg123.dll to the folder where you installed Caesar 3
4. Run Julius

**Note:** If you install Caesar 3 using Steam and plan to use Steam to launch the game,
***do not*** rename `julius.exe` to `c3.exe`.
Doing so will make the mouse cursor disappear when using right-click to scroll.
   
Instead, open `SierraLauncher.ini` and replace `Game1Exe=c3.exe` with the `Game1Exe=julius.exe`.

Alternatively, you can check the `Disable right click to drag the map` option do disable right-click scrolling.

## Windows XP

Julius still works on Windows XP, but the most recent version of SDL may not work. To use an older version of SDL that's known to work:

1. Follow the general instructions for Windows
2. Download [SDL 2.0.9](http://libsdl.org/release/SDL2-2.0.9-win32-x86.zip)
3. Extract `SDL2.dll` from that zip file to the same folder where you installed Julius, overwriting the existing file
4. Run Julius
