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
