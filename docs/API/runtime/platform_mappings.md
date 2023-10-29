# platform_mappings

These are the current platform categorizations (args.gtk.platform_mappings):

```ruby
{
  "Mac OS X"   => [:desktop, :macos, :osx, :mac, :macosx], # may also include :steam and :steam_desktop run via steam
  "Windows"    => [:desktop, :windows, :win],              # may also include :steam and :steam_desktop run via steam
  "Linux"      => [:desktop, :linux, :nix],                # may also include :steam and :steam_desktop run via steam
  "Emscripten" => [:web, :wasm, :html, :emscripten],       # may also include :touch if running in the web browser on mobile
  "iOS"        => [:mobile, :ios, :touch],
  "Android"    => [:mobile, :android, :touch],
  "Steam Deck" => [:steamdeck, :steam_deck, :steam],
}
```

Given the mappings above, `args.gtk.platform? :desktop` would return `true` if the game is running on a player's computer irrespective of the OS (MacOS, Linux, and Windows are all categorized as :desktop platforms).

