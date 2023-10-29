# parse_json

Given a json string, this function returns a hash representing the json data.

```ruby
sh = args.gtk.parse_json '{ "name": "John Doe", "aliases": ["JD"] }'
```

The above example will return a hash with the following structure: { "name"=>"John Doe", "aliases"=>["JD"] }
