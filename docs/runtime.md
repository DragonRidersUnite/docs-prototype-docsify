# Runtime

The ***GTK::Runtime*** class is the core of DragonRuby. It is globally accessible via ***$gtk*** or inside of the ***tick*** method through args.

## Example

```ruby
def tick args
  args.gtk # accessible like this
  $gtk # or like this
end
```
