# benchmark(definition)

| Parameter | Class |
| --- | --- |
| Definition | Hash |


You can use this function to compare the relative performance of blocks of code.  The only parameter is a Hash containing a key called `iterations` which represents
the number of times it should run each test.  Then a series of keys associated with a lambda function which performs the specific test you want the timing on. 
Once called, each lambda is executed  `iterations` times and a report is displayed in the DragonRuby console.

## Example

```ruby
def tick args
  # press r to run benchmark
  if args.inputs.keyboard.key_down.r
    args.gtk.console.show
    args.gtk.benchmark iterations: 1000, # number of iterations
                       # label for experiment
                       using_numeric_map: -> () {
                         # experiment body
                         v = 100.map_with_index do |i|
                           i * 100
                         end
                       },
                       # label for experiment
                       using_numeric_times: -> () {
                         # experiment body
                         v = []
                         100.times do |i|
                           v << i * 100
                         end
                       }
  end
end
```

## Related Functions

[show_console](show_console.md)
