# notify_extended!(message)

| Parameter | Class |
| --- | --- |
| message | Hash |

Has similar behavior as notify! except you have additional options to show messages in a production environment.

## Example

```ruby
def tick args
  if args.inputs.mouse.click
    args.gtk.notify_extended! message: "message",
                              duration: 300,
                              env: :prod
  end
end
```

## Related Functions

[production?](production.md), [notify!](notify.md)
