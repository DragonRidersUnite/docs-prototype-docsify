# framerate_diagnostics_primitives

Returns a set of primitives that can be rendered to the screen which provide more detailed information about the speed of your simulation (framerate, draw call count, mouse position, etc).

## Example

```ruby
def tick args
  args.outputs.primitives << args.gtk.framerate_diagnostics_primitives
end
```

## Related Functions

[current_framerate](current_framerate.md)
