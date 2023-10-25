# class ArgumentError

| | |
|---|---|
| Ancestors:| [StandardError](standarderror.md) < [Exception](exception.md) < [Object](object.md) |

Raised when the arguments are wrong and there isn’t a more specific [Exception](execption.md) class.

## Example 1: Passing the wrong number of arguments

The following code:

> `[1, 2, 3].first(4, 5)`

will trigger this exception:

> `ArgumentError: wrong number of arguments (given 2, expected 1)`


## Example 2: Passing an argument that is not acceptable

> `[1, 2, 3].first(-4)`

the negative number being an invalid argument will trigger this response:

> `ArgumentError: negative array size`

