# append_file( file_path, contents )

| Parameter | Class |
| --- | --- |
| file_path | String |
| contents | String |


Given a **file_path** and **contents**, the contents will be appended to the specified file.  If the file does not exist, it will be created and then the contents appended.  This method will write only to the sandboxed file system for the game.

## Example

```ruby
def log_entry message
  $gtk.append_file "log.txt", message
end
```

## Related Functions

[append_file_root](append_file_root.md), [write_file](write_file.md)
