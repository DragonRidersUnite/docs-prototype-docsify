# reset 
Resets DragonRuby's internal state as if it were just started. `args.state.tick_count` is set to 0 and `args.state` is cleared of any values. This function is helpful when you are developing your game and want to reset everything as if the game just booted up.

```ruby
def tick args
end

# reset the game if this file is hotloaded/required
# (removes the need to press "r" when a file is updated)
$gtk.reset
```

!> NOTE: `args.gtk.rese`t does not reset global variables or instance of classes you have have constructed. If you want to also reset global variables or instances of classes when $gtk.reset is called. Define a reset method. Here's an example:

```ruby
class Game
  def initialize
    puts "Game initialize called"
  end
end

def tick args
  $game ||= Game.new

  if args.state.tick_count == 0
    puts "tick_count is 0"
  end

  # if r is pressed on the keyboard, reset the game
  if args.inputs.keyboard.key_down.r
    args.gtk.reset
  end
end

# custom reset function
def reset
  puts "Custom reset function was called."
  $game = nil
end
```

## Related Functions

[production?](production.md), [reset_next_tick](reset_next_tick.md)
