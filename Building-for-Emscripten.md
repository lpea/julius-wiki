## Prerequisites

**Note:** In order to build Julius for Emscripten, you'll need to install and `git` and `emsdk`.

1. Installing `git`:

    a. For a Debian-based Linux distribution, open a `Terminal` window and type
       `sudo apt install git`

    b. For Mac OS, follow [installing the command line developer tools](Building-for-MacOS#installing-the-command-line-developer-tools)
       in the Mac OS section

    c. For Windows, follow [installing Git for Windows](Building-for-Windows#installing-git-for-windows-optional)
       in the Windows section

2. Installing `emsdk`.

    a. Open a Console window and navigate to the directory where you want 


## Building Julius

1. Open a `Terminal` window.

2. Navigate to the directory where you want the repository folder to be installed.
   As an example, we're using the `home` folder:

        $ cd ~

3. Clone the Julius github repository to your computer:

        $ git clone https://github.com/bvschaik/julius.git

4. Move to the new `julius` directory:

        $ cd julius

    **Optional:** If you have already downloaded the Julius repository and only wish to
    update it (in order to build a newer version), instead of the previous three steps,
    do the following in a terminal window:

    a. Move to the `julius` directory where the repository was installed.

    b. Type:

            $ git pull origin master

    c. Delete the `build` directory:

            $ rm -rf build

    d. Proceed to step 5.


5. Create a `build` directory and move to it:

        $ mkdir build && cd build

7. Run `cmake`:

        $ cmake -DCMAKE_BUILD_TYPE=Release -DTARGET_PLATFORM=emscripten -DEMSCRIPTEN_LOAD_SDL_PORTS=1 ..

    Note the special `EMSCRIPTEN_LOAD_SDL_PORTS`. If you don't add that option, cmake will search
    for SDL2, SDL2_mixer and libmpg123 libraries built by yourself, which are a hassle to compile
    for emscripten on your own.

8. Build Julius:

        $ make

5. Create the `build` directory and configure `cmake`:

        $ mkdir build && cd build && cmake -DCMAKE_BUILD_TYPE=Release -DTARGET_PLATFORM=emscripten -DEMSCRIPTEN_LOAD_SDL_PORTS=1 ..



7. Build Julius:

        $ docker exec vitasdk /bin/bash -c "cd build && make"

**Success!** Julius should have been built without any errors. There should be a file called
`julius.vpk` in the `build` folder.

See [running Julius on Vita](https://github.com/bvschaik/julius/blob/master/doc/RUNNING.md#vita) in order to install Julius to the Playstation Vita.
