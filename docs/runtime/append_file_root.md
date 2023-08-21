# append_file_root( file_path, contents )

Given a **file_path** and **contents**, the contents will be appended to the specified file.  If the file does not exist, it will be created and then the contents appended.  While in development, the **file_path** may point to a location outside of the game directory.  However, in production, this method will write to the same sandboxed location as write_file.

## Example
```ruby
def log_entry message
  $gtk.append_file_root "log.txt", message
end
```
