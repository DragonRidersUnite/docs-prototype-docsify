# parse_xml

Given xml data as a string, this function will return a hash that represents the xml data in the following recursive structure:

```ruby
{
type: :element,
name: "Person",
children: [...]
}
```
