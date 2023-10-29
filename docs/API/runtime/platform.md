# platform?

You can ask DragonRuby which platform your game is currently being run on. This can be useful if you want to perform different pieces of logic based on where the game is running.

The raw platform string value is available via `args.gtk.platform` which takes in a symbol representing the platform's categorization/mapping.

You can see all available platform categorizations via the `args.gtk.platform_mappings` function.

Here's an example of how to use `args.gtk.platform? category_symbol`:

```ruby
def tick args
  label_style = { x: 640, y: 360, anchor_x: 0.5, anchor_y: 0.5 }
  if    args.gtk.platform? :macos
    args.outputs.labels << { text: "I am running on MacOS.", **label_style }
  elsif args.gtk.platform? :win
    args.outputs.labels << { text: "I am running on Windows.", **label_style }
  elsif args.gtk.platform? :linux
    args.outputs.labels << { text: "I am running on Linux.", **label_style }
  elsif args.gtk.platform? :web
    args.outputs.labels << { text: "I am running on a web page.", **label_style }
  elsif args.gtk.platform? :android
    args.outputs.labels << { text: "I am running on Android.", **label_style }
  elsif args.gtk.platform? :ios
    args.outputs.labels << { text: "I am running on iOS.", **label_style }
  elsif args.gtk.platform? :touch
    args.outputs.labels << { text: "I am running on a device that supports touch (either iOS/Android native or mobile web).", **label_style }
  elsif args.gtk.platform? :steam
    args.outputs.labels << { text: "I am running via steam (covers both desktop and steamdeck).", **label_style }
  elsif args.gtk.platform? :steam_deck
    args.outputs.labels << { text: "I am running via steam on the Steam Deck (not steam desktop).", **label_style }
  elsif args.gtk.platform? :steam_desktop
    args.outputs.labels << { text: "I am running via steam on desktop (not steam deck).", **label_style }
  end
end
```
