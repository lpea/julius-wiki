Julius supports some command-line options. Its usage is:

    $ julius [ARGUMENTS] [DATA_DIR]

`[ARGUMENTS]` can be any combination of the following:

* `--display-scale NUMBER`

    Optional. Scales the entire Julius application by a factor of `NUMBER`. Useful for high-dpi systems.

    `NUMBER`can be any number between `0.5` and `5`. The default is `1`.

    Starting with Julius 1.6.0 this can also be set in the [configuration options](Configuration#display-scale).

* `--cursor-scale NUMBER`

    Optional. Scales the mouse cursor by a factor of `NUMBER`. Cursor scaling is independent of display scaling.

    `NUMBER` can only be set to `1`, `1.5` or `2`. The default is `1`.

    Starting with Julius 1.6.0 this can also be set in the [configuration options](Configuration#cursor-scale).

* `--windowed`

    Optional. Forces Julius to start in windowed mode

`[DATA_DIR]` Is the location of the Caesar 3 asset files.

If `[DATA_DIR]` is not provided, Julius will try to load the asset files from the directory where it is installed.

If the files are not found, it will check if a previous valid directory was stored in the internal preferences
and load the asset files from that directory.

If Julius still fails to load the assets, it will ask you to point to a valid directory.
