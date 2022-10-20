To get the Caesar 3 files from the GOG or CD-ROM version of the game, either use the Caesar3Unpacker utility or extract the files yourself using the command line.

## Use Caesar3Unpacker

1. Download the latest version of [Caesar3Unpacker](https://github.com/bvschaik/caesar3unpacker/releases/latest), open it and follow the steps in the wizard
2. Start Julius, and point the game to the folder that was just extracted

## Extract the files using the command line

### GOG: using InnoExtract

1. Install InnoExtract through [Homebrew](https://brew.sh/):
   ```
   $ brew install innoextract
   ```
2. Download the Caesar 3 offline installer exe from GOG
3. Extract the setup file to a new `app` folder:
   ```
   $ innoextract -m setup_caesar3_2.0.0.9.exe
   ```
4. Start Julius, and point the game to the `app` folder that was just extracted

### CD-ROM: using UnShield

1. Install Unshield through [Homebrew](https://brew.sh/):
   ```
   $ brew install unshield
   ```
2. Open a Terminal in the directory where you want the Caesar 3 files
3. Insert your CD-ROM and run the following command to extract the installer (replace `{CD}` with the name of your C3 cd-rom):
   ```
   $ unshield -g Exe x /Volumes/{CD}/data1.cab
   ```
4. Copy sound and video files over to the Exe directory:
   ```
   $ cp -r /Volumes/{CD}/555 Exe
   $ cp -r /Volumes/{CD}/SMK Exe
   $ cp -r /Volumes/{CD}/wavs Exe
   $ cp -r /Volumes/{CD}/Soundfx/* Exe/wavs
   ```
5. Start Julius, and point the game to the `Exe` folder that was just extracted

## Running Julius

You may get a dialog saying Julius can't be opened because it was created by an unidentified developer:

1. Locate `julius` in Applications folder (or wherever you installed it) using Finder
2. Right-click on it and choose "open"
3. You will be presented with similar-looking dialog, but this time there will be second button allowing you to run the application
4. After that you will be able to start Julius without this trick

Or: you can prevent this from happening by running the command: `xattr -d com.apple.quarantine ~/Downloads/julius*.dmg` before mounting the image (or `xattr -dr com.apple.quarantine /Applications/julius.app` (or wherever you installed it) after installing).