## Prerequisites

**Note:** In order to build Julius for the PS Vita, you'll need to install `docker` and `git`.

Instead of docker you can directly use [VitaSDK](https://vitasdk.org), but its installation
and configuration are beyond the scope of this page.

1. Installing `git`:

    a. For a Debian-based Linux distribution, open a `Terminal` window and type
       `sudo apt install git`

    b. For Mac OS, follow [installing the command line developer tools](Building-for-MacOS#installing-the-command-line-developer-tools)
       in the Mac OS section

    c. For Windows, follow [installing Git for Windows](Building-for-Windows#installing-git-for-windows-optional)
       in the Windows section

2. To install `docker`, check [installing `docker`](Installing-Docker).


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

5. Obtain the proper `docker` image for Vita development.

        $ docker run -d --name vitasdk --workdir /build/git -v "${PWD}:/build/git" gnuton/vitasdk-docker:20210217 tail -f /dev/null

6. Use `docker` to create the `build` directory and configure `cmake`:

        $ docker exec vitasdk /bin/bash -c "mkdir build && cd build && cmake -DCMAKE_BUILD_TYPE=Release -DTARGET_PLATFORM=vita .."

7. Build Julius using `docker`:

        $ docker exec vitasdk /bin/bash -c "cd build && make"

**Success!** Julius should have been built without any errors. There should be a file called
`julius.vpk` in the `build` folder.

See [running Julius on Vita](https://github.com/bvschaik/julius/blob/master/doc/RUNNING.md#vita) in order to install Julius to the Playstation Vita.
