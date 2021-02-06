OpenBSD, FreeBSD and several Linux distributions provide Julius as package. On Linux you can also use the provided [AppImage](https://appimage.org/):

1. Obtain the game data files of Caesar 3 by checking the next section.
2. Download the [latest AppImage release](https://github.com/bvschaik/julius/releases/latest) of Julius.
3. Make the downloaded AppImage executable by going into the file properties or running
   `chmod +x julius-*.AppImage` in the same folder as the AppImage.
4. You can then run it just like any Linux executable.
5. (Optional) You can install [AppImageLauncher](https://github.com/TheAssassin/AppImageLauncher#readme)
   in order to integrate the AppImage in your OS. You'll then be able to launch it easily from the menu
   just like other apps.

## Getting the Caesar 3 files

### GOG version with InnoExtract
If you bought the GOG edition, you can download the offline installer exe, and use
[InnoExtract](http://constexpr.org/innoextract/) to extract the game files:

1. Build Julius or install using your package manager
2. [Install](http://constexpr.org/innoextract/install) `innoextract` for your distribution
3. Download the Caesar 3 offline installer exe from GOG
4. Run the following command to extract the game files to a new `app` directory:

        $ innoextract -m setup_caesar3_2.0.0.9.exe

5. Move the `julius` executable to the extracted `app` directory and run from there, OR run Julius
   with the path to the game files as parameter:

        $ julius path-to-app-directory

Note that your user requires write access to the directory containing the game files, since the
saved games are also stored there.

### CD-ROM: using UnShield

1. Build Julius or install using your package manager
2. Install `unshield` for your distribution
3. Mount your CD-ROM and run the following command to extract the installer (replace `{CD}` with the path to your C3 cd-rom):
   ```
   $ unshield -g Exe x {CD}/data1.cab
   ```
4. Copy sound and video files over to the Exe directory:
   ```
   $ cp -r {CD}/555 Exe
   $ cp -r {CD}/SMK Exe
   $ cp -r {CD}/wavs Exe
   $ cp -r {CD}/Soundfx/* Exe/wavs
   ```
5. Start Julius, and point the game to the `Exe` folder that was just extracted

### Using WINE

Another option is to get the game files by installing Caesar 3 using [WINE](https://www.winehq.org/):

1. Build Julius or install using your package manager
2. Install Caesar 3 using WINE, take note where the game is installed
3. Run Julius with the path where the game is installed:

        $ julius path-to-c3-directory
