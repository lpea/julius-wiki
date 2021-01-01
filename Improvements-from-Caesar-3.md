This page lists the overall improvements and changes from Caesar 3 that Julius implements. In addition, there are [optional changes](Configuration) that can be enabled on Main Menu → Options.

## General improvements and changes

### Technical changes
- The game window can be fully resized, supporting full HD and every other resolution out of the box
- Windowed mode now works properly, regardless of your desktop color depth
- In Windowed mode, scrolling works a bit differently due to technical limitations. You need to place the cursor close to the edge of the Julius window (instead of the edge of your desktop) to scroll the map
- In fullscreen mode, if you have multiple displays, the mouse cursor is constrained to the Julius window (except on Mac due to technical issues)
- Command-line options for changing display and cursor scaling to help with HiDPI monitors
- Cross-platform: support for operating systems other than Windows, such as Linux, BSD, macOS and even consoles PS Vita and Nintendo Switch
- Support for touch devices

### Keyboard/mouse changes
- Hotkeys: if you have a non-English version of the game and/or a non-US keyboard layout, hotkeys may not map to the keys you expect. Supporting all different keyboard layouts was impossible. As a result, hotkeys are now configurable through Main Menu → Options → Configure hotkeys. Upon first start, the game tries to map the keys as best as it can.
- Various new hotkeys have been added. Check Main Menu → Options → Configure hotkeys for a complete list, and check the [default hotkeys](Hotkeys)
- Scroll wheel support in file dialogs, message list, help texts and mission briefings: basically anywhere there's a scroll bar
- Escape and right-click closes most dialogs
- Double-click can be used to open files from the file dialog
- Multi-language: when using Julius with a Korean or Chinese version of the game, entering native text is now supported

### File dialog and City Construction Kit
- Files are now listed in proper alphabetical order, not by first letter only
- The limit of 100 files has been removed: all saved games/scenarios will now show up in the list
- City Construction Kit shows the minimap of the selected scenario

### Other
- Screenshot support. Default hotkey is F12 for a normal screenshot, and Ctrl + F12 for a full-city screenshot. Both are saved as PNG files in your Caesar 3 folder
- Support for high-quality [MP3 audio files](MP3-Support)
- Small tweaks to make the game a little more color-blind friendly
- Small tweaks to panel sizes to make texts in different languages fit
- Lose game dialog now plays the audio file that was present in Caesar 3 for this

## City

### Construction and map improvements
- Building on pause is possible
- Roads adjacent to a granary or access ramp now lead into the granary/access ramp, to indicate that the granary/access ramp is part of the road network
- When deleting aqueducts, the graphics of the adjacent aqueducts are adjusted immediately to match the new configuration. In Caesar 3 you have to rotate the map to update them.
- Plaza are green when trying to build them over a road with people on it. In Caesar 3 they are red but can still be placed.
- Fountains are red when they cannot be placed, but they still indicate whether that tile has reservoir access. In Caesar 3 they always showed up as green.

### Building info improvements

- "Accept none" button on granaries and warehouses: hit the little "x" button to set all resources to "Not accepting". This also includes any resources that will become available later if you open a trade route.
- Mission post and fountain show the number of workers needed
- Amphitheater now has a right-click sound
- Granary shows cart status when it's out getting food

### Walker info improvements
- Prefects are more talkative. Instead of always saying "no sign of crime around here", they now alternate between crime info and general city info, and during fights they also talk.
- Trade caravan followers now also speak
- Some enemies didn't have images in their right-click info panel, now they do

### Tooltip improvements
- Religion overlay tooltips shows which gods the house has access to
- Senate tooltip shows number of unemployed / needed workers

### Messages
- More message types contain a button to quickly go to the relevant advisor
- Messages with videos for disasters and invasions now also contain a "go to problem" button

### Advisors
- Chief: number of unemployed people is added to senate tooltip and chief advisor
- Ratings: columns are capped when the rating is equal to the target, in Caesar 3 that only happens when your rating is strictly higher than the target. Ratings below 30 are never capped.

### Top menus
- Monthly autosave can be enabled in the in-game options menu. This is not a very sophisticated feature: your city is saved every month as "autosave.sav", overwriting any previous autosave. Consider this a backup for when you accidentally close the game.
- Replay map now asks for confirmation

## Empire map

- An icon indicates whether a trade route is a sea or land route before opening trade
- Ability to change import/export settings from the empire map
- Battle marker texts are more readable by using a different font

## Editor
- The editor is integrated into Julius - [editor files are still required](Editor)
- Brush size is visible when painting terrain, indicated by a "ghost" of green tiles
- Scheduling requests for up to 30,000 denarii are now possible.
- Demand changes can be scheduled: these are changes in trade amounts that are used frequently in the campaign mission.
- A scenario can be made "open play", which means there are no rating goals, and favor does not decline every year
- Above changes also work when playing Julius-created scenarios in Caesar 3


## Bugs fixed
- Fix storage buildings getting linked when using undo. Caesar 3 already included a fix when loading a saved game with such linked storages, but the root cause has now been found and fixed
- Freeze in Carthago during large invasions: when a LOT of soldiers are fighting each other, there was a chance that the game ended up in an infinite loop due to a programming error where memory was not properly cleared. This has been fixed.
- Gatehouse roads respawning. Build a gatehouse, you get 4 road tiles for free. Remove the roads. Now rotate the map. In Caesar 3, the roads would automatically be placed back, in Julius this no longer happens.
- Building a reservoir on top of a reservoir no longer costs money
- A rare occasion where building animations were drawn on earthquake cracks was fixed
