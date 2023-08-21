# Runtime

The ***GTK::Runtime*** class is the core of DragonRuby. It is globally accessible via ***$gtk*** or inside of the ***tick*** method through ***args***.

## Example

```ruby
def tick args
  args.gtk # accessible like this
  $gtk # or like this
end
```

## Methods

|	Methods	|	Category	|
|	---	|	:---:	|
|	append_file_root	|	Developer Support Functions	|
|	argv	|	Developer Support Functions	|
|	benchmark	|	Developer Support Functions	|
|	calcspritebox	|	Developer Support Functions	|
|	cancel_recording	|	Developer Support Functions	|
|	cli_arguments	|	Developer Support Functions	|
|	current_framerate	|	Developer Support Functions	|
|	disable_console	|	Developer Support Functions	|
|	download_stb_rb(_raw)	|	Developer Support Functions	|
|	enable_console	|	Developer Support Functions	|
|	framerate_diagnostics_primitives	|	Developer Support Functions	|
|	get_base_dir	|	Developer Support Functions	|
|	get_game_dir	|	Developer Support Functions	|
|	get_game_dir_url	|	Developer Support Functions	|
|	hide_console	|	Developer Support Functions	|
|	notify_extended!	|	Developer Support Functions	|
|	notify!	|	Developer Support Functions	|
|	open_game_dir	|	Developer Support Functions	|
|	reload_history	|	Developer Support Functions	|
|	reload_history_pending	|	Developer Support Functions	|
|	reload_if_needed	|	Developer Support Functions	|
|	reset	|	Developer Support Functions	|
|	reset_next_tick	|	Developer Support Functions	|
|	reset_sprite	|	Developer Support Functions	|
|	reset_sprites	|	Developer Support Functions	|
|	show_console	|	Developer Support Functions	|
|	slowmo!	|	Developer Support Functions	|
|	start_recording	|	Developer Support Functions	|
|	start_replay	|	Developer Support Functions	|
|	stop_recording	|	Developer Support Functions	|
|	stop_replay	|	Developer Support Functions	|
|	version	|	Developer Support Functions	|
|	version_pro?	|	Developer Support Functions	|
|	warn_array_primitives!	|	Developer Support Functions	|
|	write_file_root	|	Developer Support Functions	|
|	calcstringbox	|	Environment and Utility Functions	|
|	cursor_shown?	|	Environment and Utility Functions	|
|	exec	|	Environment and Utility Functions	|
|	hide_cursor	|	Environment and Utility Functions	|
|	open_url	|	Environment and Utility Functions	|
|	platform_mappings	|	Environment and Utility Functions	|
|	platform?	|	Environment and Utility Functions	|
|	production?	|	Environment and Utility Functions	|
|	quit_requested?	|	Environment and Utility Functions	|
|	request_quit	|	Environment and Utility Functions	|
|	set_cursor	|	Environment and Utility Functions	|
|	set_mouse_grab	|	Environment and Utility Functions	|
|	set_system_cursor	|	Environment and Utility Functions	|
|	set_window_fullscreen	|	Environment and Utility Functions	|
|	set_window_scale	|	Environment and Utility Functions	|
|	show_cursor	|	Environment and Utility Functions	|
|	system	|	Environment and Utility Functions	|
|	window_fullscreen?	|	Environment and Utility Functions	|
|	append_file	|	File IO Functions	|
|	delete_file	|	File IO Functions	|
|	delete_file_if_exist	|	File IO Functions	|
|	list_files	|	File IO Functions	|
|	read_file	|	File IO Functions	|
|	stat_file	|	File IO Functions	|
|	write_file	|	File IO Functions	|
|	dlopen	|	Indie and Pro Functions	|
|	get_pixels	|	Indie and Pro Functions	|
|	http_get	|	Network IO Functions	|
|	http_post	|	Network IO Functions	|
|	http_post_body	|	Network IO Functions	|
|	start_server!	|	Network IO Functions	|
|	parse_json	|	XML and JSON	|
|	parse_json_file	|	XML and JSON	|
|	parse_xml	|	XML and JSON	|
|	parse_xml_file	|	XML and JSON	|
