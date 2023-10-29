# set_window_fullscreen

This function takes in a single boolean parameter. true to make the game fullscreen, false to return the game back to windowed mode.

```ruby
def tick args
  # make the game full screen after 600 frames (10 seconds)
  if args.state.tick_count == 600
    args.gtk.set_window_fullscreen true
  end

  # return the game to windowed mode after 20 seconds
  if args.state.tick_count == 1200
    args.gtk.set_window_fullscreen false
  end
end
```
