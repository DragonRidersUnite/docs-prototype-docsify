# warn_array_primitives!

This function helps you audit your game of usages of array-based primitives. While array-based primitives are simple to create and use, they are slower to process than Hash or Class based primitives.

```ruby
def tick args
  # enable array based primitives warnings
  args.gtk.warn_array_primitives!

  # array-based primitive elsewhere in code
  # an log message will be posted giving the location of the array
  # based primitive usage
  args.outputs.sprites << [100, 100, 200, 200, "sprites/square/blue.png"]

  # instead of using array based primitives, migrate to hashes as needed
  args.outputs.sprites << {
    x: 100,
    y: 100,
    w: 200,
    h: 200, path:
    "sprites/square/blue.png"
  }
end
```

