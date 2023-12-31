# args.outputs

DragonRuby calls anything that can be rendered to the screen a **primitive** which can be defined using *Arrays, Hashes* and *Classes*.  Primitives can be of the type: border, label, line, solid or sprite.

`Outputs` is how you render primitives to the screen. The minimal setup for rendering something to the screen is through a tick method defined in `mygame/app/main.rb`

```ruby
def tick args
  args.outputs.solids     << [0, 0, 100, 100]
  args.outputs.sprites    << [100, 100, 100, 100, "sprites/square/blue.png"]
  args.outputs.labels     << [200, 200, "Hello World"]
  args.outputs.lines      << [300, 300, 400, 400]
end
```

## Render Order

Primitives are rendered first-in, first-out. The rendering order (sorted by bottom-most to top-most):

1. solids
1. sprites
1. primitives: Accepts all render primitives. Useful when you want to bypass the default rendering orders for rendering (eg. rendering solids on top of sprites).
1. labels
1. lines
1. borders
1. debug: Accepts all render primitives. Use this to render primitives for debugging (production builds of your game will not render this layer)


## solids

Add primitives to this collection to render a *filled geometric shape* to the screen.  Currently, only quads and triangles (with the Indie/Pro version) are supported.


### Using an Array

Creates a solid black rectangle located at 100, 100. 160 pixels wide and 90 pixels tall.

```ruby
def tick args
  #                         X    Y  WIDTH  HEIGHT
  args.outputs.solids << [100, 100,   160,     90]
end
```

### Using an Array with colors and alpha

The value for the color and alpha is a number between 0 and 255. The alpha property is optional and will be set to 255 if not specified.

Creates a green solid rectangle with an opacity of 50%.

```ruby
def tick args
  #                         X    Y  WIDTH  HEIGHT  RED  GREEN  BLUE  ALPHA
  args.outputs.solids << [100, 100,   160,     90,   0,   255,    0,   128]
end
```

### Using a Hash

If you want a more readable invocation. You can use the following hash to create a solid. Any parameters that are not specified will be given a default value. The keys of the hash can be provided in any order.

```ruby
def tick args
  args.outputs.solids << {
    x:    0,
    y:    0,
    w:  100,
    h:  100,
    r:    0,
    g:  255,
    b:    0,
    a:  255,
    anchor_x: 0,
    anchor_y: 0,
    blendmode_enum: 1
  }
end
```

### Using a Class

You can also create a class with solid properties and render it as a primitive. ALL properties must be on the class. *Additionally*, a method called primitive_marker must be defined on the class.

Here is an example:

```ruby
# Create type with ALL solid properties AND primitive_marker
class Solid
  attr_accessor :x, :y, :w, :h, :r, :g, :b, :a, :anchor_x, :anchor_y, :blendmode_enum

  def primitive_marker
    :solid # or :border
  end
end

# Inherit from type
class Square < Solid
  # constructor
  def initialize x, y, size
    self.x = x
    self.y = y
    self.w = size
    self.h = size
  end
end

def tick args
  # render solid/border
  args.outputs.solids  << Square.new(10, 10, 32)
end
```


## borders

Add primitives to this collection to render an unfilled solid to the screen. Take a look at the documentation for Outputs#solids.

The only difference between the two primitives is where they are added.

Instead of using `args.outputs.solids`:

```ruby
def tick args
  #                         X    Y  WIDTH  HEIGHT
  args.outputs.solids << [100, 100,   160,     90]
end
```

You have to use `args.outputs.borders`:

```ruby
def tick args
  #                           X    Y  WIDTH  HEIGHT
  args.outputs.borders << [100, 100,   160,     90]
end
```

## sprites

Add primitives to this collection to render a sprite to the screen.

### Using an Array

Creates a sprite of a white circle located at 100, 100. 160 pixels wide and 90 pixels tall.

```ruby
def tick args
  #                         X    Y   WIDTH   HEIGHT                      PATH
  args.outputs.sprites << [100, 100,   160,     90, "sprites/circle/white.png]
end
```

### Using an Array with colors and alpha

The value for the color and alpha is a number between 0 and 255. The alpha property is optional and will be set to 255 if not specified.

Creates a green circle sprite with an opacity of 50%.

```ruby
def tick args
  #                         X    Y  WIDTH  HEIGHT           PATH                ANGLE  ALPHA  RED  GREEN  BLUE
  args.outputs.sprites << [100, 100,  160,     90, "sprites/circle/white.png",     0,    128,   0,   255,    0]
end
```

### Using a Hash

If you want a more readable invocation. You can use the following hash to create a sprite. Any parameters that are not specified will be given a default value. The keys of the hash can be provided in any order.

```ruby
def tick args
  args.outputs.sprites << {
    x:                             0,
    y:                             0,
    w:                           100,
    h:                           100,
    path: "sprites/circle/white.png",
    angle:                         0,
    a:                           255,
    r:                             0,
    g:                           255,
    b:                             0
  }
end
```

### Using a Class

You can also create a class with solid/border properties and render it as a primitive. ALL properties must be on the class. *Additionally*, a method called primitive_marker must be defined on the class.

Here is an example:

```ruby
# Create type with ALL sprite properties AND primitive_marker
class Sprite
attr_accessor :x, :y, :w, :h, :path, :angle, :a, :r, :g, :b, :tile_x,
              :tile_y, :tile_w, :tile_h, :flip_horizontally,
              :flip_vertically, :angle_anchor_x, :angle_anchor_y, :id,
              :angle_x, :angle_y, :z,
              :source_x, :source_y, :source_w, :source_h, :blendmode_enum,
              :source_x2, :source_y2, :source_x3, :source_y3, :x2, :y2, :x3, :y3,
              :anchor_x, :anchor_y

  def primitive_marker
    :sprite
  end
end

# Inherit from type
class Circle < Sprite
# constructor
  def initialize x, y, size, path
    self.x = x
    self.y = y
    self.w = size
    self.h = size
    self.path = path
  end

  def serialize
    {x:self.x, y:self.y, w:self.w, h:self.h, path:self.path}
  end

  def inspect
    serialize.to_s
  end

  def to_s
    serialize.to_s
  end
end

def tick args
  # render circle sprite
  args.outputs.sprites  << Circle.new(10, 10, 32,"sprites/circle/white.png")
end
```

## labels

Add primitives to this collection to render a label.

### Using an Array 

Labels represented as Arrays/Tuples:

```ruby
def tick args
                         #        X         Y              TEXT   SIZE_ENUM
  args.outputs.labels << [175 + 150, 610 - 50, "Smaller label.",         0]
end
```

Here are all the properties that you can set with a label represented as an Array. It's recommended to move over to using Hashes once you've specified a lot of properties.

```ruby
def tick args
  args.outputs.labels << [
    640,                   # X
    360,                   # Y
    "Hello world",         # TEXT
    0,                     # SIZE_ENUM
    1,                     # ALIGNMENT_ENUM
    0,                     # RED
    0,                     # GREEN
    0,                     # BLUE
    255,                   # ALPHA
    "fonts/coolfont.ttf"   # FONT
  ]
end
```

### Using a Hash

```ruby
def tick args
  args.outputs.labels << {
      x:                       200,
      y:                       550,
      text:                    "dragonruby",
      size_enum:               2,
      alignment_enum:          1, # 0 = left, 1 = center, 2 = right
      r:                       155,
      g:                       50,
      b:                       50,
      a:                       255,
      font:                    "fonts/manaspc.ttf",
      vertical_alignment_enum: 0  # 0 = bottom, 1 = center, 2 = top
  }
end
```


## Screenshots

Add a hash to this collection to take a screenshot and save as png file. The keys of the hash can be provided in any order.

```ruby
def tick args
  args.outputs.screenshots << {
    x: 0, y: 0, w: 100, h: 100,    # Which portion of the screen should be captured
    path: 'screenshot.png',        # Output path of PNG file (inside game directory)
    r: 255, g: 255, b: 255, a: 0   # Optional chroma key
  }
end
```

### Chroma key (Making a color transparent)

By specifying the r, g, b and a keys of the hash you change the transparency of a color in the resulting PNG file. This can be useful if you want to create files with transparent background like spritesheets. The transparency of the color specified by r, g, b will be set to the transparency specified by a.

The example under the Screenshots shows the color white (255, 255, 255) as chroma key which will set all white pixels to have a 0 alpha channel.
