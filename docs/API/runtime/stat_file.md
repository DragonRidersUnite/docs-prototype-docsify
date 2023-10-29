# stat_file 

This function takes in one parameter. The parameter is the file path and assumes the the game directory is the root. The method returns nil if the file doesn't exist otherwise it returns a Hash with the following information:

```ruby
# {
#   path: String,
#   file_size: Int,
#   mod_time: Int,
#   create_time: Int,
#   access_time: Int,
#   readonly: Boolean,
#   file_type: Symbol (:regular, :directory, :symlink, :other),
# }

def tick args
  if args.inputs.mouse.click
    args.gtk.write_file "last-mouse-click.txt", "Mouse was clicked at #{args.state.tick_count}."
  end

  file_info = args.gtk.stat_file "last-mouse-click.txt"

  if file_info
    args.outputs.labels << {
      x: 30,
      y: 30.from_top,
      text: file_info.to_s,
      size_enum: -3
    }
  else
    args.outputs.labels << {
      x: 30,
      y: 30.from_top,
      text: "file does not exist, click to create file",
      size_enum: -3
    }
  end
end
```
