# set_cursor

Replaces the mouse cursor with a sprite. Takes in a path to the sprite, and optionally an x and y value representing the realtive positioning the sprite will have to the mouse cursor.

```ruby
def tick args
  if args.state.tick_count == 0
    # assumes a sprite of size 80x80 and centers the sprite
    # relative to the cursor position.
    args.gtk.set_cursor "sprites/square/blue.png", 40, 40
  end
end
```
