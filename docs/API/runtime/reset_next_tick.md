# reset_next_tick

Has the same behavior as reset except the reset occurs before tick is executed again. reset resets the environment immediately (while the tick method is inflight). It's recommended that reset should be called outside of the tick method (invoked when a file is saved/hotloaded), and reset_next_tick be used inside of the tick method so you don't accidentally blow away state the your game depends on to complete the current tick without exceptions.

```ruby
def tick args
  # reset the game if "r" is pressed on the keyboard
  if args.inputs.keyboard.key_down.r
    args.gtk.reset_next_tick # use reset_next_tick instead of reset
  end
end

# reset the game if this file is hotloaded/required
# (removes the need to press "r" when I file is updated)
$gtk.reset
```

## Related Functions

[production?](production.md), [reset](reset.md)
