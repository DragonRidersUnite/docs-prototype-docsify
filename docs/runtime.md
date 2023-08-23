# Runtime

The **GTK::Runtime** class is the core of DragonRuby. It is globally accessible via **$gtk** or inside of the **tick** method through **args**.

## Example

```ruby
def tick args
  args.gtk # accessible like this
  $gtk # or like this
end
```
## Functions

### Application

| Function | Description |
| --- | --- |
|	argv	|		|
|	cli_arguments	|		|
|	quit_requested?	|	Returns true if a request to quit the Application was made.	|
|	request_quit	|	Makes a request for DragonRuby to clean up the Application process and quit to the operating system.	|
				
### Debugging & Development

| Function | Description |
| --- | --- |
|	benchmark	|		|
|	production?	|	Returns true if the DragonRuby Application is running as a Production release.	|
|	current_framerate	|		|
|	disable_console	|		|
|	download_stb_rb(_raw)	|		|
|	enable_console	|		|
|	framerate_diagnostics_primitives	|		|
|	hide_console	|		|
|	notify_extended!	|		|
|	notify!	|		|
|	open_game_dir	|		|
|	reload_history	|		|
|	reload_history_pending	|		|
|	reload_if_needed	|		|
|	reset	|		|
|	reset_next_tick	|		|
|	reset_sprite	|		|
|	reset_sprites	|		|
|	show_console	|		|
|	slowmo!	|		|
|	version	|		|
|	version_pro?	|		|
|	warn_array_primitives!	|		|
				
### Dragon Replay

| Function | Description |
| --- | --- |
|	cancel_recording	|		|
|	start_recording	|		|
|	start_replay	|		|
|	stop_recording	|		|
|	stop_replay	|		|
				
### File I/O	

| Function | Description |
| --- | --- |
|	append_file	|	Adds content to the end of an existing file.	|
|	append_file_root	|	Adds content to the end of an existing file.	|
|	delete_file	|	Removes a file from the OS file system.	|
|	delete_file_if_exist	|	Removes a file from the OS file system.	|
|	get_base_dir	|		|
|	get_game_dir	|		|
|	get_game_dir_url	|		|
|	list_files	|	Returns an array of filenames in a given path.	|
|	read_file	|	Returns the contents of a file as a String.	|
|	stat_file	|	Returns a Hash containing statistics about the given file.	|
|	write_file	|	Creates/Overwrites a given file with the supplied contents.	|
|	write_file_root	|		|
				
### Indie & Pro Features

| Function | Description |
| --- | --- |
|	get_pixels	|		|
|	dlopen	|		|
				
### JSON & XML Data

| Function | Description |
| --- | --- |
|	parse_json	|	Converts JSON data from a String into a Hash.	|
|	parse_json_file	|	Converts JSON data from a File into a Hash.	|
|	parse_xml	|	Converts XML data from a String into a Hash.	|
|	parse_xml_file	|	Converts XML data from a File into a Hash.	|
				
### Mouse

| Function | Description |
| --- | --- |
|	cursor_shown?	|	Returns true if the Mouse Cursor is visible.	|
|	hide_cursor	|	Turns the Mouse Cursor invisible.	|
|	set_cursor	|	Sets the sprite used for the Mouse Cursor.	|
|	set_mouse_grab	|	Sets the Grab mode of the Mouse Cursor.	|
|	set_system_cursor	|	Changes the appearance of the Mouse Cursor using system cursors.	|
|	show_cursor	|	Turns the Mouse Cursor visible.	|
				
### Network I/O

| Function | Description |
| --- | --- |
|	http_get	|		|
|	http_post	|		|
|	http_post_body	|		|
|	start_server!	|		|
				
### Operating System

| Function | Description |
| --- | --- |
|	exec	|	Executes a OS shell command and returns result in a string.	|
|	open_url	|	Opens the URL in user’s default browser.	|
|	platform_mappings	|	A hash of attributes related to each OS platform.	|
|	platform?	|	The OS platform that DragonRuby is currently running on.	|
|	system	|	Executes a OS shell command and returns result to the console.	|
				
### String

| Function | Description |
| --- | --- |
|	calcstringbox	|	Returns the pixel dimensions of a String should it be rendered in a font.	|
				
### Window

| Function | Description |
| --- | --- |
|	set_window_fullscreen	|	Sets the game to Fullscreen or Windowed modes.	|
|	set_window_scale	|	Sets a scaling factor for the Window.	|
|	window_fullscreen?	|	Returns true if the Window is currently in Fullscreen mode.	|




