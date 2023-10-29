# start_replay

Given a file that represents a recording, this method will run the recording against the current codebase.

You can start a replay from the command line also:

```
first argument: the game directory
--replay switch is the file path relative to the game directory
--speed switch is optional. a value of 4 will run the replay and game at 4x speed
cli command example is in the context of Linux and Mac, for Windows the binary would be ./dragonruby.exe
dragonruby ./mygame --replay ./replay.txt --speed 4
```
