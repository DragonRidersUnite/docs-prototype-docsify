# start_server!

Starts a in-game http server that can be process http requests. When your game is running in development mode. A dev server is started at http://localhost:9001

You can start an in-game http server in production via:

```ruby
def tick args
  # server explicitly enabled in production
  args.gtk.start_server! port: 9001, enable_in_prod: true
end
Here's how you would responde to http requests:

def tick args
  # server explicitly enabled in production
  args.gtk.start_server! port: 9001, enable_in_prod: true

  # loop through pending requests and respond to them
  args.inputs.http_requests.each do |request|
    puts "#{request}"
    request.respond 200, "ok"
  end
end
```
