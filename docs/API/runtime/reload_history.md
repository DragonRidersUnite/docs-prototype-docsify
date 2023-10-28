# reload_history

Returns a Hash representing the code files that have be loaded for your game along with timings for the events. This should be used for development/debugging purposes only.

## Example Output

```ruby
{
  "app/main.rb" => {
    : current => {
      : path => "app/main.rb",: global_at => -1,: event =>: reload_completed
    },: history => [{
      : path => "app/main.rb",
      : global_at => -1,
      : event =>: reload_queued
    }, {
      : path => "app/main.rb",
      : global_at => -1,
      : event =>: processing
    }, {
      : path => "app/main.rb",
      : global_at => -1,
      : event =>: reload_completed
    }]
  }, ...
}
```

## Related Functions

[production?](production.md), [reload_history_pending](reload_history_pending.md)
