# delete_file

This function takes in a single parameters. The parameter is the file path that should be deleted. This function will raise an exception if the path requesting to be deleted does not exist.

**Notes:**
* Use delete_if_exist to only delete the file if it exists.
* Use stat_file to determine if a path exists.
* Use list_files to determine if a directory is empty.
* You cannot delete files outside of your sandboxed game environment.

Here is a list of reasons an exception could be raised:

- If the path is not found.
- If the path is still open (for reading or writing).
- If the path is not a file or directory.
- If the path is a circular symlink.
- If you do not have permissions to delete the path.
- If the directory attempting to be deleted is not empty.

```ruby
def tick args
  if args.inputs.mouse.click
    args.gtk.write_file "last-mouse-click.txt", "Mouse was clicked at #{args.state.tick_count}."
  end
end
```
