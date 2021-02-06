To run Julius on Nintendo Switch, follow these steps:

1. Ensure you have a jailbroken Switch. Detailed jailbreaking instructions can be found on
   [Nintendo Homebrew's Guide](https://nh-server.github.io/switch-guide/) or, alternatively, on
   [AtlasNX's Guide](https://guide.teamatlasnx.com/).
2. Extract the contents of `julius-switch.zip` into the `switch` folder on your SD card,
   so that you have a folder `/switch/julius` with `julius.nro` inside.
3. Copy all the files from a Caesar 3 install into the `/switch/julius/` folder, so that you
   have the file `/switch/julius/c3.eng` and more.

## Controls

| Input                                          | Effect                                                       |
| ---------------------------------------------- | ------------------------------------------------------------ |
| Left Analog Stick                              | Move the mouse pointer                                       |
| Right Analog Stick or Dpad Up/Down/Left/Right  | Scroll the map                                               |
| R / A                                          | Left mouse button                                            |
| L / B                                          | Right mouse button                                           |
| ZR                                             | Hold to slow down analog stick mouse pointer                 |
| ZL                                             | Hold to speed up analog stick mouse pointer                  |
| X                                              | Simulate Page Up keypress (speed up in-game time)            |
| Y                                              | Simulate Page Down keypress (slow down in-game time)         |
| Plus                                           | Bring up on-screen keyboard, useful to enter player name etc.|
| Minus                                          | Toggle between touch modes                                   |

Touch modes can be toggled with the minus button. There are three modes:
1. Touchpad mode (default)
    * Single finger drag = move the mouse pointer (indirectly like on a touchpad)
    * Single short tap = left mouse click
    * Single short tap while holding a second finger down = right mouse click
2. Direct mode
    * Pointer jumps to finger, nothing else
3. [Julius mode](Touch-Support)

For multi-touch gestures, the fingers have to be far enough apart from each other, so that the
Switch will not erroneously recognize them as a single finger. Otherwise the pointer will jump around.

Physical USB mice and keyboards are supported. All keyboards seem to work. Not all mice work.
A mouse compatibility list is available
[here](https://docs.google.com/spreadsheets/d/1Drbo5-QuSX901MwtOytSMuqRGxeIkq2HELM806I9dj0/edit#gid=0)
