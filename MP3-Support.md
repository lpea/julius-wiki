Julius supports the playback of MP3 files instead of the original, low-quality wav files.

If you have the high-quality MP3 files that were once available from the Sierra Website, you can play them instead of the original files. Alternatively, you can play any MP3 file you like instead of the original music.

[Download the original five city background MP3 files](https://bintray.com/bvschaik/caesar3-music/mp3#files).

## Requirements

In order to play the files, you must have the library `libmpg123-0` installed. If you installed Julius using one of the official releases, `libmpg123-0` is already installed.

When building from source, `libmpg123-0` is usually installed with `SDL_mixer`. If not, you can install it using your package manager.

## Where to place the MP3 files

Create a folder named `mp3` in the main folder where your Caesar 3 data files are. In this folder, place some or all of the following files:

* `ROME1.mp3` - City background music, population 0 to 1000
* `ROME2.mp3` - City background music, population 1000 to 2000
* `ROME3.mp3` - City background music, population 2000 to 5000
* `ROME4.mp3` - City background music, population 5000 to 7000
* `ROME5.mp3` - City background music, population 7000+
* `Combat_Long.mp3` - Battle music, 32 or more invaders on the map
* `Combat_Short.mp3` - Short battle music, 1-31 invaders on the map
* `setup.mp3` - Main menu music

For each file that is missing, Julius will play the original `.wav` instead.
