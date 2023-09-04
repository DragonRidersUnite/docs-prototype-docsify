# Ruby API

DragonRuby's goal is to be compliant with the ISO/IEC 30170:2012 standard. It's syntax is Ruby 2.x compatible, but also contains semantic changes that help it natively interface with platform specific libraries.

DragonRuby supports a subset of MRI apis. Our target is to support all of mRuby's standard lib. There are challenges to this given the number of platforms we are trying to support (specifically console).

## Classes
| Name | Inherits | Modules | Description |
|---|---|---|---|
|	ArgumentError	|	StandardError	|		|		|
|	Array	|	Object	|	Enumerable	|		|
|	EOFError	|	IOError	|		|		|
|	Enumerator	|	Object	|		|		|
|	Exception	|	Object	|		|		|
|	FalseClass	|	Object	|		|		|
|	Fiber	|	Object	|		|		|
|	File	|	IO	|	Constants	|		|
|	FileTest	|	Object	|		|		|
|	Fixnum	|	Integer	|		|		|
|	Float	|	Numeric	|		|		|
|	FloatDomainError	|	RangeError	|		|		|
|	FrozenError	|	RuntimeError	|		|		|
|	Hash	|	Object	|	Enumerable	|		|
|	IO	|	Object	|		|		|
|	IOError	|	StandardError	|		|		|
|	IndexError	|	StandardError	|		|		|
|	Integer	|	Numeric	|		|		|
|	KeyError	|	IndexError	|		|		|
|	LocalJumpError	|	ScriptError	|		|		|
|	Method	|	Object	|		|		|
|	Module	|	Object	|		|		|
|	NameError	|	StandardError	|		|		|
|	NilClass	|	Object	|	NilClassFalseClass	|		|
|	NoMemoryError	|	Exception	|		|		|
|	NoMethodError	|	NameError	|		|		|
|	NotImplementedError	|	ScriptError	|		|		|
|	Numeric	|	Object	|	Comparable, ValueType	|		|
|	Object	|		|		|		|
|	Proc	|	Object	|		|		|
|	Random	|	Object	|		|		|
|	Range	|	Object	|	Enumerable	|		|
|	RangeError	|	StandardError	|		|		|
|	RegexpError	|	StandardError	|		|		|
|	ScriptError	|	Exception	|		|		|
|	StandardError	|	Exception	|		|		|
|	StopIterationError	|	IndexError	|		|		|
|	String	|	Object	|	Comparable, ValueType	|		|
|	Struct	|	Object	|		|		|
|	Symbol	|	Object	|	Comparable, ValueType	|		|
|	SystemStackError	|	Exception	|		|		|
|	Time	|	Object	|	Comparable	|		|
|	TrueClass	|	Object	|	ValueType	|		|
|	TypeError	|	StandardError	|		|		|
|	UnboundMethod	|	Object	|		|		|


## Modules
| Name | Description |
|---|---|
|	BasicObject	|		|
|	Comparable	|		|
|	Enumerable	|		|
|	Kernel	|		|
|	Math	|		|
|	NilClassFalseClass	|		|
|	ValueType	|		|


