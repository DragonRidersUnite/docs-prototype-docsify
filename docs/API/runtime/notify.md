# notify!( message )

| Parameter | Class |
| --- | --- |
| message | String |

Given a string, this function will present a message at the bottom of your game. This method is only invoked in development mode and is useful for debugging.

An optional parameter of duration (number value representing ticks) can also be passed in. The default value of 300 ticks (5 seconds).

## Example

```ruby
def tick args
  if args.inputs.mouse.click
    args.gtk.notify! "Mouse was clicked!"
  end

  if args.inputs.keyboard.key_down.r
    # optional duration parameter
    args.gtk.notify! "R key was pressed!", 600 # present message for 10 seconds/600 frames
  end
end

```

## Related Functions

[production?](production.md), [notify_extended!](notify_extended.md)
