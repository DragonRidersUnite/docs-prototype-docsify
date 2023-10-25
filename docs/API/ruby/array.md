# class Array

| | |
|---|---|
| Ancestors:| [Object](object.md) |
| Modules: | [Enumerable](enumerable.md) |

An Array is an ordered, integer-indexed collection of objects, called elements. Any object (even another array) may be an array element, and an array can contain objects of different types.

The Array class has been extended to provide methods that will help in common game development tasks. Array is one of the most powerful classes in Ruby and a very fundamental component of Game Toolkit.

## Class Methods

| Method | Parameters | Description |
| --- | --- | --- |
| [] | *args | Returns a new array populated with the given objects (args) |
| new | | Returns a new empty array |
| new | array | Returns a new array formed from the array parameter |
| new | size | Returns a new array with size elements containing nil |
| new | size, default | Returns a new array with size elements each containing the default value |
| new | size {\|index\| } | Returns a new array with size elements each containing the return value of the block function | 
| try_convert | object | Returns an array created from object. Returns nil or throws an exception, if it fails. |

## Operator Methods

| Method | Parameters | Description |
| --- | --- | --- |
| & | other_array | Returns a new Array containing distinct elements from both arrays. Elements are compared using eql? |
| * | n | When non-negative argument Integer n is given, returns a new Array built by concatenating the n copies of self |
| + | other_array |  Returns a new Array containing all elements of array followed by all elements of other_array |
| - | other_array | Returns a new Array containing only those elements from the first array that are not found in other_array; items are compared using eql?; the order from array is preserved |
| << | object | Appends object to the array |
| <=> | other_array | Returns -1, 0, or 1 as self is less than, equal to, or greater than other_array.  |
| == | other_array | Returns true if the size and elements of both arrays are equal. |
