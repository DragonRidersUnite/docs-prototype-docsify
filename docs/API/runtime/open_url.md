# open_url

Given a uri represented as a string. This fuction will open the uri in the user's default browser.

```ruby
def tick args
  # open a url after 600 frames (10 seconds)
  if args.state.tick_count == 600
    args.gtk.open_url "http://dragonruby.org"
  end
end
```
