# calcstringbox

Returns the render width and render height as a tuple for a piece of text. The parameters this method takes are:

* text: the text you want to get the width and height of.
* size_enum: number representing the render size for the text. This parameter is optional and defaults to 0 which represents a baseline font size in units specific to DragonRuby (a negative value denotes a size smaller than what would be comfortable to read on a handheld device postive values above 0 represent larger font sizes).
* font: path to a font file that the width and height will be based off of. This field is optional and defaults to the DragonRuby's default font.

```ruby
def tick args
  text = "a piece of text"
  size_enum = 5 # "large font size"

  # path is relative to your game directory (eg mygame/fonts/courier-new.ttf)
  font = "fonts/courier-new.ttf"

  # get the render width and height
  string_w, string_h = args.gtk.calcstringbox text, size_enum, font

  # render the label
  args.outputs.labels << {
    x: 100,
    y: 100,
    text: text,
    size_enum: size_enum,
    font: font
  }

  # render a border around the label based on the results from calcstringbox
  args.outputs.borders << {
    x: 100,
    y: 100,
    w: string_w,
    h: string_h,
    r: 0,
    g: 0,
    b: 0
  }
end
```
