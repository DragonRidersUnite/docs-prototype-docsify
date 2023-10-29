# reload_history_pending

Returns a Hash for files that have been queued for reload, but haven't been processed yet. This should be used for development/debugging purposes only.

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

[production?](production.md), [reload_history](reload_history.md), [reload_if_needed](reload_if_needed.md)
