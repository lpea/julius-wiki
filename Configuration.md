Julius provides a number of configuration settings that can fix bugs present in Caesar 3 and change the user interface a bit. You can access the configuration through the "Options" button on the main menu.

## User interface changes

### Play intro videos

Checking this option will play the three intro videos when the game starts.

### Extra information in the control panel

Checking this option will show extra information in the Control Panel (sidebar) when you are in the city. Depending on your resolution, this will show:

- Game speed controls
- Unemployment info
- Rating info

[[images/config-sidebar-info.png]]

### Enable smooth scrolling

Checking this option will scroll the city map in a smoother way: it will scroll by pixel instead of by full tile.

### Improve visual feedback when clearing land

Checking this option will highlight buildings in red when hovering over them when the "clear land" tool is selected.

### Allow building each temple in succession

Checking this option will add an "All" option to the build menu of small and large temples. Using this will allow you to place the temples to the gods in order without having to re-select the temple from the build menu. Placement order is the following: Ceres, Neptune, Mercury, Mars, Venus.

### Show range when building reservoirs, fountains and wells

Checking this option will allow you to preview the range of reservoirs, fountains and wells when building them:

[[images/config-water-preview.png]]

### Show draggable construction size

Checking this option will display the size when building draggable items, such as roads and houses, allowing you to easily measure the amount of items you want to place:

[[images/config-construction-size.png]]

## Gameplay changes

### Fix immigration bug on very hard

In Caesar 3, if you play on Very Hard difficulty level, people will get upset with you by default when your population is at least 200. However, any conditions in your city that might improve their happiness, such as no employment, high wages, etc, will not have any effect until your population reaches 300. This means that people will leave your city and you'll never reach 300. This can be overcome by ensuring there is a large number of immigrants on the way to bump you from 200 to over 300 population.

When you check this option, people will not get unhappy until your population reaches 300.

### Fix 100-year-old ghosts

In Caesar 3, when people reach 100 in the census, they are removed from the total population, but still occupy a slot in one of the houses. When you are building eternal cities that last for hundreds of years, these so-called "ghosts" accumulate until your city no longer functions. The only way to prevent ghosts is to prevent people from reaching 100 years old by keeping city health poor.

Checking this option fixes this such that no new ghosts will be created.

### Fix Emperor change and survival time in custom missions

In Caesar 3 custom missions, the Change of Emperor event does not do anything other than triggering a message, even though the manual states that favor should be reset to 50.
For survival time missions, the survival time only works properly when no other win criteria have been set. If there are any other win criteria, the player wins the mission when they are met, instead of having to play until the end of the survival time.

Checking this option will reset favor to 50 on Change of Emperor events, and will force the player to play until the survival time when win criteria have been met.

## Language packs

If you have another language version of the game, you can add it to Julius and easily switch between languages within the game.

To add a language pack:

1. Create a new folder inside your Caesar 3 installation with the name of the language. It doesn't really matter how you name it, as long as it only contains Latin letters (a-z)
1. Add the localized files to this folder: the `.eng` files, and optionally create a `wavs` subfolder for the sound files, and a `smk` subfolder for the video files
1. Start the game, go to Options and select your language folder. To reset it back to your default language, select "(default)"
