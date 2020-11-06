To build Julius, you'll need:

- a compiler: `gcc`, `clang`, Visual Studio and MinGW(-w64) are all known to be supported
- `git`
- `cmake`
- `SDL2`
- `SDL2_mixer`
- `libpng` - optional, a bundled copy will be used if not found

After cloning the repo, run the following commands:

	$ mkdir build && cd build
	$ cmake ..
	$ make

This results in a `julius` executable.

See [Running Julius](https://github.com/bvschaik/julius/blob/master/doc/RUNNING.md) for instructions on how to configure Julius for your platform.

## CMake options

- `-DSYSTEM_LIBS=OFF` - use the bundled copies of optional libraries even if a system version is available
- `-DVITA_BUILD=ON` - build for Vita
- `-DSWITCH_BUILD=ON` - build for Switch
- `-DANDROID_BUILD=ON` - build for Android

## Detailed instructions

For detailed building instructions, please check out the respective page:

- [Building for Windows](Building-for-Windows)
- [Building for Linux](Building-for-Linux)
- [Building for Mac](Building-for-MacOS)
- [Building for Playstation Vita](Building-for-Vita)
- [Building for Nintendo Switch](Building-for-Switch)
- [Building for Android](Building-for-Android)
