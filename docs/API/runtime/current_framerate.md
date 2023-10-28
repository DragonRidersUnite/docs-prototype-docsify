# current_framerate

Returns a float value representing the framerate of your game. This is an approximation/moving average of your framerate and should eventually settle to 60fps.

## Example

```ruby
def tick args
  # render a label to the screen that shows the current framerate
  # formatted as a floating point number with two decimal places
  args.outputs.labels << { x: 30, y: 30.from_top, text: "#{args.gtk.current_framerate.to_sf}" }
end
```

## Related Functions

[framerate_diagnostics_primitives](framerate_diagnostics_primitives.md)
