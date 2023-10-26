# class ArgumentError

| | |
|---|---|
| Ancestors:| [StandardError](standarderror.md) < [Exception](exception.md) < [Object](object.md) |

Raised when the arguments are wrong and there isn’t a more specific [Exception](exception.md) class.

### Example 1: Passing the wrong number of arguments

The following code:

```ruby 
 [1, 2, 3].first(4, 5)
```

will trigger this exception:

```
 ArgumentError: wrong number of arguments (given 2, expected 1)
```


### Example 2: Passing an invalid argument

The negative number being passed to the first() method:

```ruby
 [1, 2, 3].first(-4)
```

 will trigger this response:

```
 ArgumentError: negative array size
```

