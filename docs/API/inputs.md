# args.inputs

Access using input using `args.inputs`.

### last_active

This function returns the last active input which will be set to either :keyboard, :mouse, or :controller. The function is helpful when you need to present on screen instructions based on the input the player chose to play with.

```ruby
def tick args
  if args.inputs.last_active == :controller
    args.outputs.labels << { x: 60, y: 60, text: "Use the D-Pad to move around." }
  else
    args.outputs.labels << { x: 60, y: 60, text: "Use the arrow keys to move around." }
  end
end
```

`:mouse`, or `:controller`. The function is helpful when you need to present on screen instructions based on the input the player chose to play with.

### locale

Returns the ISO 639-1 two-letter langauge code based on OS preferences. Refer to the following link for locale strings: https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes).

Defaults to "en" if locale can't be retrieved (args.inputs.locale_raw will be nil in this case).

### up

Returns true if: the up arrow or w key is pressed or held on the keyboard; or if up is pressed or held on controller_one; or if the left_analog on controller_one is tilted upwards.

### down

Returns true if: the down arrow or s key is pressed or held on the keyboard; or if down is pressed or held on controller_one; or if the left_analog on controller_one is tilted downwards.

### left

Returns true if: the left arrow or a key is pressed or held on the keyboard; or if left is pressed or held on controller_one; or if the left_analog on controller_one is tilted to the left.

### right

Returns true if: the right arrow or d key is pressed or held on the keyboard; or if right is pressed or held on controller_one; or if the left_analog on controller_one is tilted to the right.

### left_right

Returns -1 (left), 0 (neutral), or +1 (right) depending on results of `args.inputs.left` and `args.inputs.right`.

`args.state.player[:x] += args.inputs.left_right * args.state.speed`

### up_down

Returns -1 (down), 0 (neutral), or +1 (up) depending on results of `args.inputs.down` and `args.inputs.up`.

`args.state.player[:y] += args.inputs.up_down * args.state.speed`

### text

Returns a string that represents the last key that was pressed on the keyboard.

## Mouse (args.inputs.mouse)

Represents the user's mouse.

| Properties | Description |
| --- | --- |
| has_focus | Return's true if the game has mouse focus.|
| x | Returns the current x location of the mouse.|
| y | Returns the current y location of the mouse.|
| moved | Returns true if the mouse has moved on the current frame.|
|button_left | Returns true if the left mouse button is down.|
|button_middle |Returns true if the middle mouse button is down.|
| button_right | Returns true if the right mouse button is down.|
| button_bits  | Returns a bitmask for all buttons on the mouse: 1 for a button in the down state, 0 for a button in the up state.|
| wheel | Represents the mouse wheel. Returns nil if no mouse wheel actions occurred. Otherwise `args.inputs.mouse.wheel` will return a Hash with `x`, and `y` (representing movement on each axis).|
| click OR down, previous_click, up | The properties args.inputs.mouse.(click|down|previous_click|up) each return nil if the mouse button event didn't occur. And return an Entity that has an x, y properties along with helper functions to determine collision: inside_rect?, inside_circle. This value will be true if any of the mouse's buttons caused these events. To scope to a specific button use .button_left, .button_middle, .button_right, or .button_bits.|

| Methods | Arguments | Description |
| --- | --- | --- |
| inside_rect? | rec | Return. args.inputs.mouse.inside_rect? takes in any primitive that responds to `x`, `y`, `w`, `h` |
| inside_circle? | center_point, radius | Returns true if the mouse is inside of a specified circle. `args.inputs.mouse.inside_circle?` takes in any primitive that responds to `x`, `y` (which represents the circle's center), and takes in a `radius`. |


## Touch 

The following touch apis are available on touch devices (iOS, Android, Mobile Web, Surface).

| Properties | Description |
| --- | --- |
| touch | Returns a Hash representing all touch points on a touch device.|
| finger_left | Returns a Hash with x and y denoting a touch point that is on the left side of the screen.|
| finger_right | Returns a Hash with x and y denoting a touch point that is on the right side of the screen.|


## Controller (args.inputs.controller_(one-four))

Represents controllers connected to the usb ports.

| Properties | Description |
| --- | --- |
| active | Returns true if any of the controller's buttons were used. |
| up | Returns true if up is pressed or held on the directional or left analog.|
| down | Returns true if down is pressed or held on the directional or left analog.|
| left | Returns true if left is pressed or held on the directional or left analog.|
| right | Returns true if right is pressed or held on the directional or left analog. |
| left_right | Returns -1 (left), 0 (neutral), or +1 (right) depending on results of `args.inputs.controller_(one-four).left` and `args.inputs.controller_(one-four).right`.|
| up_down | Returns -1 (down), 0 (neutral), or +1 (up) depending on results of `args.inputs.controller_(one-four).up` and `args.inputs.controller_(one-four).down`.|
| (left|right)_analog_x_raw | Returns the raw integer value for the analog's horizontal movement (-32,000 to +32,000).|
| (left|right)_analog_y_raw | Returns the raw integer value for the analog's vertical movement (-32,000 to +32,000).|
| (left|right)_analog_x_perc | Returns a number between -1 and 1 which represents the percentage the analog is moved horizontally as a ratio of the maximum horizontal movement.|
|(left|right)_analog_y_perc | Returns a number between -1 and 1 which represents the percentage the analog is moved vertically as a ratio of the maximum vertical movement.|
| directional_up | Returns true if up is pressed or held on the directional.|
| directional_down | Returns true if down is pressed or held on the directional.|
| directional_left | Returns true if left is pressed or held on the directional.|
| directional_right | Returns true if right is pressed or held on the directional.|
| ( a| b| x| y| l1| r1| l2| r2| l3| r3| start| select ) | Returns true if the specific button is pressed or held.|
|truthy_keys |Returns a collection of Symbols that represent all keys that are in the pressed or held state.|
|key_down | Returns true if the specific button was pressed on this frame. `args.inputs.controller_(one-four).key_down.BUTTON` will only be true on the frame it was pressed.|
| key_held | Returns true if the specific button is being held. `args.inputs.controller_(one-four).key_held.BUTTON` will be true for all frames after `key_down` (until released).|
|key_up | Returns true if the specific button was released. `args.inputs.controller_(one-four).key_up.BUTTON` will be true only on the frame the button was released.|

## Keyboard (args.inputs.keyboard) 

Represents the user's keyboard.

| Properties | Description |
| --- | --- |
| active | Returns true if any keys on the keyboard were pressed. |
| has_focus | Returns true if the game has keyboard focus. |
| up | Returns true if up or w is pressed or held on the keyboard.|
| down | Returns true if down or s is pressed or held on the keyboard.|
| left | Returns true if left or a is pressed or held on the keyboard.|
| right | Returns true if right or d is pressed or held on the keyboard.|
|left_right | Returns -1 (left), 0 (neutral), or +1 (right) depending on results of `args.inputs.keyboard.left` and `args.inputs.keyboard.right`.|
|up_down | Returns -1 (left), 0 (neutral), or +1 (right) depending on results of `args.inputs.keyboard.up` and `args.inputs.keyboard.up`.|

### keyboard properties 

The following properties represent keys on the keyboard and are available on `args.inputs.keyboard.KEY`, `args.inputs.keyboard.key_down.KEY`, `args.inputs.keyboard.key_held.KEY`, and `args.inputs.keyboard.key_up.KEY`:

* alt
* meta
* control
* shift
* ctrl_KEY (dynamic method, eg args.inputs.keyboard.ctrl_a)
* exclamation_point
* zero - nine
* backspace
* delete
* escape
* enter
* tab
* (open|close)_round_brace
* (open|close)_curly_brace
* (open|close)_square_brace
* colon
* semicolon
* equal_sign
* hyphen
* space
* dollar_sign
* double_quotation_mark
* single_quotation_mark
* backtick
* tilde
* period
* comma
* pipe
* underscore
* a - z
* shift
* control
* alt
* meta
* left
* right
* up
* down
* pageup
* pagedown
* char
* plus
* at
* forward_slash
* back_slash
* asterisk
* less_than
* greater_than
* carat
* ampersand
* superscript_two
* circumflex
* question_mark
* section_sign
* ordinal_indicator
* raw_key
* left_right
* up_down
* directional_vector
* truthy_keys

### keys
Returns a Hash with all keys on the keyboard in their respective state. The Hash contains the following keys

* `:down`
* `:held`
* `:down_or_held`
* `:up`
