# slowmo!

Given a numeric value representing the factor of 60fps. This function will bring your simulation loop down to a slower rate. This method is intended to be used for debugging purposes.

```ruby
def tick args
  # set your simulation speed to (15 fps): args.gtk.slowmo! 4
  # set your simulation speed to (1 fps): args.gtk.slowmo! 60
  # set your simulation speed to (30 fps):
  args.gtk.slowmo! 2
end
```

Removing this line from your tick method will automatically set your simulation speed back to 60 fps.

## Related Functions

[production?](production.md)

