# argv

Returns a string representing the full command line and arguments passed to the DragonRuby binary. This should be used for development/debugging purposes only.

## Example

If you started DragonRuby with the shell command `./dragonruby` then the following code will output that string.

```ruby
  puts $gtk.argv
```
