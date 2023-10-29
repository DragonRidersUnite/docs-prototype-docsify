# get_game_dir

Returns the location within sandbox storage that the game is running. When developing your game, this value will be your mygame directory. In production, it'll return a value that is OS specific (eg the Roaming directory on Windows or the Application Support directory on Mac).

Invocations of [write_file](write_file.md) or [append_file](append_file.md) will write to this sandboxed directory.
