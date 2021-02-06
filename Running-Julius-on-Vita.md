To run Julius on PlayStation Vita, follow these steps:

1. Ensure you have a jailbroken Vita. Detailed jailbreaking instructions can be found on
   [vita.hacks.guide](https://vita.hacks.guide).
2. Install the `julius.vpk` file using Vitashell, like any other homebrew.
3. Copy all the files from a Caesar 3 install into a folder `ux0:/data/julius/`, so that you
   have the file `ux0:/data/julius/c3.eng` and more in your folder.

## Controls

| Input                                          | Effect                                                       |
| ---------------------------------------------- | ------------------------------------------------------------ |
| Left Analog Stick                              | Move the mouse pointer                                       |
| Right Analog Stick or Dpad Up/Down/Left/Right  | Scroll the map                                               |
| R / Cross                                      | Left mouse button                                            |
| L / Circle                                     | Right mouse button                                           |
| Triangle                                       | Simulate Page Up keypress (speed up in-game time)            |
| Square                                         | Simulate Page Down keypress (slow down in-game time)         |
| Start                                          | Bring up on-screen keyboard, useful to enter player name etc.|
| Select                                         | Toggle between touch modes                                   |

Touch modes can be toggled with the select button. There are three modes:
1. Touchpad mode (default)
    * Single finger drag = move the mouse pointer (indirectly like on a touchpad)
    * Single short tap = left mouse click
    * Single short tap while holding a second finger down = right mouse click
2. Direct mode
    * Pointer jumps to finger, nothing else
3. [Julius mode](Touch-Support)

For multi-touch gestures, the fingers have to be far enough apart from each other, so that the
Vita will not erroneously recognize them as a single finger. Otherwise the pointer will jump around.

Physical Bluetooth mice and keyboards are supported. This was tested with the "Jelly Comb Mini Bluetooth
Keyboard With Mouse Touchpad," and with the "Jelly Comb Bluetooth Wireless Mouse." The Vita doesn't pair
with all Bluetooth devices.
