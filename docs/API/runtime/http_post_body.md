# http_post_body

Returns an object that represents an http response which will eventually have a value. This http_post_body method is invoked asynchronously. Check for completion before attempting to read results.

* First parameter: The url to send the request to.
* Second parameter: String that represents the body that will be sent
* Third parameter: Headers. Be sure to populate the Content-Type that matches the data you are sending.

```ruby
def tick args
  # perform an http get and print the response when available

  args.state.json ||= "{ "userId": "#{Time.now.to_i}"}"
  args.state.result ||= args.gtk.http_post_body "http://httpbin.org/post",
                                                args.state.json,
                                                ["Content-Type: application/json", "Content-Length: #{args.state.json.length}"]


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
