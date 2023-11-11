# Command-Line Tools

## dragonruby \[folder location\]

This tool is the heart of DragonRuby.  It is the Virtual Machine that executes your DragonRuby code.  By default, it doesn't need any options passed to it as long as it was installed from the downloaded ZIP file and the game you want to execute is contained in the `mygames` folder.

<br>

## dragonruby-publish \[options\] game_directory

This is tool has several options that allow you to package your game quickly for all supported platforms.  See the Deployment guides for instructions on how to publish to some of the more intricate platforms.

| Option | Required? | Description |
|---|---|---|
| --package| N | |
| --package-with-remote-hotload | N | |
| game_directory | Y | |

<br>

## dragonruby-bind \[options\] input_file

This tool is used to help create extensions for DragonRuby.  It takes a C source code file as input and produces another C source code file as output.  The output file contains a new set of functions that bind to mRuby. 
Once compiled, this allows DragonRuby to call these C functions directly from your Ruby code.

| Option | Required? | Description |
|---|---|---|
| --version | N | Displays various versions and attributes that dragonruby will use to produce the new bindings. |
| --help | N | Displays the available options |
| --help-list | N | Displays the available options |
| --compiler-flags=\<string\>| N | Flags to pass to the compiler |
| --ffi-module=\<string\> | N | Module under which attach FFI bindings |
| --no-argument-check | N | Do not emit code for argument checks |
| --no-typecheck | N | Do not emit code for typechecks |
| --output=\<string\> | N | Output file (default stdout) |
| --register=\<string\> | N | Registration function name |

<br>

### Examples

**Version Example**
```
./dragonruby-bind --version
```
Outputs the following on a Macbook Air:
```
LLVM (http://llvm.org/):
  LLVM version 10.0.0
  Optimized build.
  Default target: x86_64-apple-darwin22.6.0
  Host CPU: cyclone
```

<br>

**Output Example**

The following commandline examples show how to create a binding from a C source file named `ext.c` and output a `ext-bind.c` file for both Linux/MacOS and Windows.
```
./dragonruby-bind --output=mygame/ext-bind.c mygame/ext.c

.\dragobruby-bind.exe --output=mygame\ext-bind.c mygame\ext.c
```

