# Ruby API

DragonRuby's goal is to be compliant with the ISO/IEC 30170:2012 standard. It's syntax is Ruby 2.x compatible, but also contains semantic changes that help it natively interface with platform specific libraries.

DragonRuby supports a subset of MRI APIs. Our target is to support all of mRuby's [standard lib](https://mruby.org/docs/api/_index.html). There are challenges to this given the number of platforms we are trying to support (specifically console).

Below are a list of Classes that DragonRuby has modified to add support for game development.

### Classes
| Name | Inherits | Modules | Description |
|---|---|---|---|
|	[Array](ruby/array.md)	|	Object|	Enumerable|	An ordered, integer-indexed collection of objects. |
|	[Numeric](ruby/numeric.md)	|	Object |	Comparable , ValueType	|		|


### Modules
| Name | Description |
|---|---|
|	[Kernel](ruby/kernel.md)	|	The Kernel module is included by class Object, so its methods are available in every Ruby object.	|



