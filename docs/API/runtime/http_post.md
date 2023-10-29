# http_post

Returns an object that represents an http response which will eventually have a value. This http_post method is invoked asynchronously. Check for completion before attempting to read results.

* First parameter: The url to send the request to.
* Second parameter: Hash that represents form fields to send.
* Third parameter: Headers. Note: Content-Type must be form encoded flavor. If you are unsure of what to pass in, set the content type to application/x-www-form-urlencoded

```ruby
def tick args
  # perform an http get and print the response when available

  args.state.form_fields ||= { "userId" => "1697452243" }
  args.state.result ||= args.gtk.http_post "http://httpbin.org/post",
                                           args.state.form_fields,
                                           ["Content-Type: application/x-www-form-urlencoded"]


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
