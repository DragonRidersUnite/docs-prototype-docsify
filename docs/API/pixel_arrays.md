# args.pixel_arrays

Pixel arrays allow you to dynamically create new sprites.  They are closely related to Render Targets but allow access to the individual pixels of your PixelArray.  A PixelArray has a `width`, `height` and an Array of `pixels` which contain hexadecimal color values in the **ABGR** format.

You can create a pixel array like this:

```ruby
w = 200
h = 100
args.pixel_array(:my_pixel_array).w = w
args.pixel_array(:my_pixel_array).h = h
```

You'll also need to fill the pixels with values, if they are nil, the array will render with the checkerboard texture. You can use `#00000000` to fill with transparent pixels if desired.  The following code will clear the pixel array to a solid green color.

```ruby
gs.pixel_array(:my_pixel_array).pixels.fill #FF00FF00, 0, w * h
```

!> Note: To convert from rgb hex (like skyblue #87CEEB) to abgr hex, you split it in pairs pair (eg 87 CE EB) and reverse the order (eg EB CE 87) add join them again: #EBCE87. Then add the alpha component in front ie: FF for full opacity: #FFEBCE87.


Your pixel array can be drawn through the outputs like other primitves.  Pixel arrays are considered `sprite` primitives and must be rendered using the `sprites` outputs.  
Instead of referencing a an image file path, set the `:path` to the symbol of your pixel array as shown in the following example.

```ruby
args.outputs.sprites << { x: 500, y: 300, w: 200, h: 100, path: :my_pixel_array) }
```

To find the color value stored at a specific `x`, `y` position, you can index the `pixels` array as if it were a bottom-left coordinate system like this:

```ruby
x = 150
y = 33
args.pixel_array(:my_pixel_array).pixels[(height - y) * width + x] = 0xFFFFFFFF
```


## Related Sample Apps

Animation using pixel arrays: `./samples/07_advanced_rendering/06_pixel_arrays`

Load a pixel array from a png: `./samples/07_advanced_rendering/06_pixel_arrays_from_file/`
