# cli_arguments

Returns a Hash for command line arguments in the format of --switch value (two hyphens preceding the switch flag with the value seperated by a space). This should be used for development/debugging purposes only.

## Example

The following code:

```ruby
  puts $gtk.cli_arguments
```
will result in the following output:

```
{:dragonruby=>"mygame"}
```

## Related Functions

[argv](argv.md)
