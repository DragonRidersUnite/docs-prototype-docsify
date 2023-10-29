# system

Given an OS dependent cli command represented as a string, this function executes the command and puts the results to the DragonRuby Console (returns nil).

```ruby
def tick args
  # execute ls on the current directory in 10 seconds
  if args.state.tick_count == 600
    args.gtk.system "ls ."
  end
end
```
