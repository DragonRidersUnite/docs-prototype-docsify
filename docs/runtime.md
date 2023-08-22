# Runtime

The **GTK::Runtime** class is the core of DragonRuby. It is globally accessible via **$gtk** or inside of the **tick** method through **args**.

## Example

```ruby
def tick args
  args.gtk # accessible like this
  $gtk # or like this
end
```

## Developer Support

|| Functions |
|:---:|---|
| A | [append_file_root](/docs/runtime/append_file_root.md), argv |
| B | benchmark |
| C | calcspritebox, cancel_recording, cli_arguments, current_framerate |
| D | disable_console, download_stb_rb(_raw) |
| E | enable_console |
| F | framerate_diagnostics_primitives |
| G | get_base_dir, get_game_dir, get_game_dir_url |
| H | hide_console |
| N | notify_extended!, notify! |
| O | open_game_dir |
| R | reload_history, reload_history_pending, reload_if_needed, reset, reset_next_tick, reset_sprite, reset_sprites |
| S | show_console, slowmo!, start_recording, start_replay, stop_recording, stop_replay |
| V | version, version_pro? |
| W | warn_array_primitives!, write_file_root |


## Environment and Utility

| Category | Functions | Description |
|:---:|---|---|
|	Application	|	production?	|	Returns true if the DragonRuby Application is running as a Production release.	|
|		|	quit_requested?	|	Returns true if a request to quit the Application was made.	|
|		|	request_quit	|	Makes a request for DragonRuby to clean up the Application process and quit to the operating system.	|
|		|		|		|
|	Mouse	|	cursor_shown?	|	Returns true if the Mouse Cursor is visible.	|
|		|	hide_cursor	|	Turns the Mouse Cursor invisible.	|
|		|	set_cursor	|	Sets the sprite used for the Mouse Cursor.	|
|		|	set_mouse_grab	|	Sets the Grab mode of the Mouse Cursor.	|
|		|	set_system_cursor	|	Changes the appearance of the Mouse Cursor using system cursors.	|
|		|	show_cursor	|	Turns the Mouse Cursor visible.	|
|		|		|		|
|	Networking	|	open_url	|	Opens the URL in user’s default browser.	|
|		|		|		|
|	Operating System	|	exec	|	Executes a OS shell command and returns result in a string.	|
|		|	platform_mappings	|	A hash of attributes related to each OS platform.	|
|		|	platform?	|	The OS platform that DragonRuby is currently running on.	|
|		|	system	|	Executes a OS shell command and returns result to the console.	|
|		|		|		|
|	String	|	calcstringbox	|	Returns the pixel dimensions of a String should it be rendered in a font.	|
|		|		|		|
|	Window	|	set_window_fullscreen	|	Sets the game to Fullscreen or Windowed modes.	|
|		|	set_window_scale	|	Sets a scaling factor for the Window.	|
|		|	window_fullscreen?	|	Returns true if the Window is currently in Fullscreen mode.	|


