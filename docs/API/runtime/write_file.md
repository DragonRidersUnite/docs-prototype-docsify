# write_file

This function takes in two parameters. The first parameter is the file path and assumes the the game directory is the root. The second parameter is the string that will be written. The method **overwrites** whatever is currently in the file. Use [append_file](append_file.md) to append to the file as opposed to overwriting.

```ruby
def tick args
  if args.inputs.mouse.click
    args.gtk.write_file "last-mouse-click.txt", "Mouse was clicked at #{args.state.tick_count}."
  end
end
```

