When contributing to the Julius source, please follow the code style used in the project. Formatting conventions will be strictly enforced in pull requests to keep the code-base uniform. Don't worry about getting them all right the first time, just open a pull request, and if anything needs to change we'll kindly point that out.

## Code formatting

For formatting, follow these rules, which are mostly the K&R style:
- Indent by 4 spaces
- For functions, opening and closing braces go on their own line
- For statements within functions: opening brace goes on the same line as the `if`, `for` or `while` statement
- Braces are mandatory, even for blocks that are only 1 statement
- One space is required between `if`, etc and their opening parenthesis, and between the closing parenthesis and the opening brace
- Switch/case statements: indent each `case` by 4 spaces, further indent the code within a `case` block by another 4 spaces
- Pointer variable declaration: the `*` goes next to the variable. Example: use `building *b;`, not `building* b;`
- Always end the file with a new line
- Keep line length to 120 characters maximum, break up longer lines to multiple lines in positions where it's logical. Indent the continuation line(s) by 4 spaces.

## File layout

The content of a C file is sorted in the following order, with a blank line between each group:

1. Include of the corresponding header, without any path prefixes
1. Includes of other files from the project using double quotes, using their full path starting relative to `src`, sorted alphabetically
1. Includes of external headers, sorted alphabetically
1. Constants declared using `#define`
1. Constants/arrays/etc declared using `static const`
1. Static function declarations
1. Static file variables. For UI-related files, first define the buttons, then the generic `data` container for other variables
1. Functions, ordered by usage. Prefer to put static functions above where they're first used

### Function order for window files

For UI window files, keep to the following order:

1. Init function, if necessary
1. Background draw function and related helper functions
1. Foreground draw function and related helper functions
1. Input handling functions and related helper functions
1. Input button click handlers
1. The `show` function

## Naming conventions

Use `snake_case` for everything. For constants, either `#define` or `const`, use `CAPITAL_SNAKE_CASE` to indicate they're constants.

 i, j, k for loops and x and y for position, use descriptive variable names

### Function names

Public functions should contain the file's location in the first part of their name to make it easy to find them. For example, the function `game_tick_run()` lives in `src/game/tick.c`.
Static function should NOT contain the file's location and should be given an appropriate name for what they do.

### Variable names

Use descriptive names, we're not on a character budget. Single-letter variables are only allowed in these cases: `i`, `j` only in `for` loops, `x` and `y` only for position variables.

Group file-scoped primitive variables together in an anonymous `data` struct so when using them it's clear they're global and not function-scoped. Example:

    static struct {
        int num_legions;
        int focus_button_id;
    } data;

## Architecture

- Try to keep the UI and game logic code as separate as possible. Ideally there should be no `#include` to either `window/` or `widget/` files in any of the other files, but it's not always possible.
- Do not references _any_ of the SDL functions in the game's code outside of the `platform/` directory. This ensures that the core of the game can run without external libraries (for testing, for example), and it doesn't tie the project to SDL. If you really need to call something provided by SDL, create a function in `game/system.h` and put the implementation in one of the files in the `platform/` directory.