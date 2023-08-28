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
|	[argv](./runtime/argv.md)	|	Returns a String of the command line parameters.	|
|	[cli_arguments](runtime/cli_arguments.md)	|	Returns a Hash of the command line parameters.	|
|	[quit_requested?](runtime/quit_requested.md)	|	Returns true if a request to quit the Application was made.	|
|	[request_quit](runtime/request_quit.md)	|	Makes a request for DragonRuby to clean up the Application process and quit to the operating system.	|
				
### Debugging & Development	

| Function | Description |
| --- | --- |		
|	[benchmark](runtime/benchmark.md)	|	Used to compare the performance of blocks of code.	|
|	[production?](runtime/production.md)	|	Returns true if the DragonRuby Application is running as a Production release.	|
|	[current_framerate](runtime/current_framerate.md)	|	Returns a float representing the moving average of the frame rate.	|
|	[disable_console](runtime/disable_console.md)	|	Disables the DragonRuby Console so that it will no longer appear.	|
|	[download_stb_rb](runtime/download_stb_rb.md)	|	Downloads a Ruby file from Github.	|
|	[download_stb_raw](runtime/download_stb_raw.md)	|	Downloads a raw file from Github.	|
|	[enable_console](runtime/enable_console.md)	|	Enables the DragonRuby Console so that it can be shown and hidden.	|
|	[framerate_diagnostics_primitives](runtime/framerate_diagnostics_primitives.md)	|	Primitives that display statistics about your DragonRuby app.	|
|	[hide_console](runtime/hide_console.md)	|	Hide the DragonRuby Console and resumes the game.	|
|	[notify_extended!](runtime/notify_extended.md)	|	Displays a message banner even in Production mode.	|
|	[notify!](runtime/notify.md)	|	Displays a message banner while in Development mode.	|
|	[open_game_dir](runtime/open_game_dir.md)	|	Opens the OS’ file manager to the location of the game directory.	|
|	[reload_history](runtime/reload_history.md)	|	Returns a Hash of the code files and their load timings.	|
|	[reload_history_pending](runtime/reload_history_pending.md)	|	Returns a Hash of files that are queued for loading.	|
|	[reload_if_needed](runtime/reload_if_needed.md)	|	Queues a file for reload, if it has been modified.	|
|	[reset](runtime/reset.md)	|	Immediately resets DragonRuby to its starting state.	|
|	[reset_next_tick](runtime/reset_next_tick.md)	|	Resets DragonRuby to its starting state by the next tick.	|
|	[reset_sprite](runtime/reset_sprite.md)	|	Invalidates a cached sprite causing it to be reloaded from disk.	|
|	[reset_sprites](runtime/reset_sprites.md)	|	Invalidates all cached sprites causing them to be reloaded.	|
|	[show_console](runtime/show_console.md)	|	Displays the DragonRuby Console.	|
|	[slowmo!](runtime/slowmo.md)	|	Divides the target frame rate by a factor to simulate slow performance.	|
|	[version](runtime/version.md)	|	Returns a String containing the DragonRuby version that is running.	|
|	[version_pro?](runtime/version_pro.md)	|	Returns True if DragonRuby can use non-Standard features.	|
|	[warn_array_primitives!](runtime/warn_array_primitives.md)	|	Logs warnings when array-based primitives are being used in your code.	|
				
### Dragon Replay	

| Function | Description |
| --- | --- |		
|	[cancel_recording](runtime/cancel_recording.md)	|	Stops and discards current gameplay recording.	|
|	[start_recording](runtime/start_recording.md)	|	Resets DragonRuby engine and starts recording gameplay.	|
|	[start_replay](runtime/start_replay.md)	|	Runs a replay recording.	|
|	[stop_recording](runtime/stop_recording.md)	|	Stops gameplay recording and writes the current session to a file.	|
|	[stop_replay](runtime/stop_replay.md)	|	Stops a currently executing replay.	|
				
### File IO	

| Function | Description |
| --- | --- |		
|	[append_file](runtime/append_file.md)	|	Adds content to the end of an existing file.	|
|	[append_file_root](/docs/runtime/append_file_root.md)	|	Adds content to the end of an existing file even outside the sandbox.	|
|	[delete_file](runtime/delete_file.md)	|	Removes a file from the OS file system.	|
|	[delete_file_if_exist](runtime/delete_file_if_exist.md)	|	Removes a file from the OS file system.	|
|	[get_base_dir](runtime/get_base_dir.md)	|	Returns the location of the DragonRuby binary.	|
|	[get_game_dir](runtime/get_game_dir.md)	|	Returns the path to the sandbox game storage location.	|
|	[get_game_dir_url](runtime/get_game_dir_url.md)	|	Returns a URL to the sandbox game storage location.	|
|	[list_files](runtime/list_files.md)	|	Returns an array of filenames in a given path.	|
|	[read_file](runtime/read_file.md)	|	Returns the contents of a file as a String.	|
|	[stat_file](runtime/stat_file.md)	|	Returns a Hash containing statistics about the given file.	|
|	[write_file](runtime/write_file.md)	|	Creates/Overwrites a given file with the supplied contents.	|
|	[write_file_root](runtime/write_file_root.md)	|	Creates/Overwrites a given file with the supplied contents even outside the sandbox.	|
				
### Indie & Pro Features	

| Function | Description |
| --- | --- |		
|	[get_pixels](runtime/get_pixels.md)	|	Loads a sprite file as a 1D-array of color values.	|
|	[dlopen](runtime/dlopen.md)	|	Loads a Dynamic Library.  Uses C-Extension feature.	|
				
### JSON & XML Data		

| Function | Description |
| --- | --- |	
|	[parse_json](runtime/parse_json.md)	|	Converts JSON data from a String into a Hash.	|
|	[parse_json_file](runtime/parse_json_file.md)	|	Converts JSON data from a File into a Hash.	|
|	[parse_xml](runtime/parse_xml.md)	|	Converts XML data from a String into a Hash.	|
|	[parse_xml_file](runtime/parse_xml_file.md)	|	Converts XML data from a File into a Hash.	|
				
### Mouse			

| Function | Description |
| --- | --- |
|	[cursor_shown?](runtime/cursor_shown.md)	|	Returns true if the Mouse Cursor is visible.	|
|	[hide_cursor](runtime/hide_cursor.md)	|	Turns the Mouse Cursor invisible.	|
|	[set_cursor](runtime/set_cursor.md)	|	Sets the sprite used for the Mouse Cursor.	|
|	[set_mouse_grab](runtime/set_mouse_grab.md)	|	Sets the Grab mode of the Mouse Cursor.	|
|	[set_system_cursor](runtime/set_system_cursor.md)	|	Changes the appearance of the Mouse Cursor using system cursors.	|
|	[show_cursor](runtime/show_cursor.md)	|	Turns the Mouse Cursor visible.	|
				
### Network IO		

| Function | Description |
| --- | --- |	
|	[http_get](runtime/http_get.md)	|	Asynchronously, returns an object representing the HTTP response to a GET request.	|
|	[http_post](runtime/http_post.md)	|	Asynchronously, returns an object representing the HTTP response to a POST request.	|
|	[http_post_body](runtime/http_post_body.md)	|	Asynchronously, returns an object representing the HTTP response to a POST request.	|
|	[start_server!](runtime/start_server!.md)	|	Opens a networking port for listening as a server.	|
				
### Operating System	

| Function | Description |
| --- | --- |		
|	[exec](runtime/exec.md)	|	Executes a OS shell command and returns result in a string.	|
|	[open_url](runtime/open_url.md)	|	Opens the URL in user’s default browser.	|
|	[platform_mappings](runtime/platform_mappings.md)	|	A hash of attributes related to each OS platform.	|
|	[platform?](runtime/platform.md)	|	The OS platform that DragonRuby is currently running on.	|
|	[system](runtime/system.md)	|	Executes a OS shell command and returns result to the console.	|
				
### String			

| Function | Description |
| --- | --- |
|	[calcstringbox](runtime/calcstringbox.md)	|	Returns the pixel dimensions of a String should it be rendered in a font.	|
				
### Window			

| Function | Description |
| --- | --- |
|	[set_window_fullscreen](runtime/set_window_fullscreen.md)	|	Sets the game to Fullscreen or Windowed modes.	|
|	[set_window_scale](runtime/set_window_scale.md)	|	Sets a scaling factor for the Window.	|
|	[window_fullscreen?](runtime/window_fullscreen.md)	|	Returns true if the Window is currently in Fullscreen mode.	|




