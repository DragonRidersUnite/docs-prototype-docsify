# exec

Given an OS dependent cli command represented as a string, this function executes the command and returns a string representing the results.

```ruby
def tick args
  # execute ls on the current directory in 10 seconds
  if args.state.tick_count == 600
    results = args.gtk.exec "ls ."
    puts "The results of the command are:"
    puts results
  end
end
```
