# request_quit

Call this function to exit your game. You will be given one additional tick if you need to perform any housekeeping before that game closes.

## Example

```ruby
def tick args
  # exit the game after 600 frames (10 seconds)
  if args.state.tick_count == 600
    args.gtk.request_quit
  end
end
```

## Related Functions

[quit_requested?](quit_requested?.md)
