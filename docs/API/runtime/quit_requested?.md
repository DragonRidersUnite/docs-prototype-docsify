# quit_requested?

This function will return true if the game is about to exit (either from the user closing the game or if [request_quit](request_quit.md) was invoked).

## Example

Once the `request_quit` has been called, there is one final tick that DragonRuby will issue before shutting down.

```ruby
def tick args
  # exit the game after 600 frames (10 seconds)
  if args.state.tick_count == 600
    args.gtk.request_quit
  end

  if quit_requested?
    # Clean Up Application before closing
  end
end
```

## Related Functions

[request_quit](request_quit.md)
