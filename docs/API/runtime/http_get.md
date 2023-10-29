# http_get

Returns an object that represents an http response which will eventually have a value. This http_get method is invoked asynchronously. Check for completion before attempting to read results.

```ruby
def tick args
  # perform an http get and print the response when available
  args.state.result ||= args.gtk.http_get "https://httpbin.org/html"

  if args.state.result && args.state.result[:complete] && !args.state.printed
    if args.state.result[:http_response_code] == 200
      puts "The response was successful. The body is:"
      puts args.state.result[:response_data]
    else
      puts "The response failed. Status code:"
      puts args.state.result[:http_response_code]
    end
    # set a flag denoting that the response has been printed
    args.state.printed = true

    # show the console
    args.gtk.show_console
  end
end
```
