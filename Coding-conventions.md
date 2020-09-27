When contributing to the Julius source, please follow the code style used in the project. Formatting conventions will be strictly enforced in pull requests to keep the code-base uniform.

## Code formatting

For formatting, follow these rules, which are mostly the K&R style:
- For functions, opening and closing braces go on their own line
- For statements within functions: opening brace goes on the same line as the `if`, `for` or `while` statement
- Braces are mandatory, even for blocks that are only 1 statement
- One space is required between `if`, etc and their opening parenthesis, and between the closing parenthesis and the opening brace
- Pointer variable declaration: the `*` goes next to the variable. Example: use `building *b;`, not `building* b;`

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

### Function names

Public functions should contain the file's location in the first part of their name to make it easy to find them. For example, the function `game_tick_run()` lives in `src/game/tick.c`.
Static function should NOT contain the file's location and should be given an appropriate name for what they do.