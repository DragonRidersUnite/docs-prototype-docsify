# Ruby API

DragonRuby's goal is to be compliant with the ISO/IEC 30170:2012 standard. It's syntax is Ruby 2.x compatible, but also contains semantic changes that help it natively interface with platform specific libraries.

DragonRuby supports a subset of MRI apis. Our target is to support all of mRuby's standard lib. There are challenges to this given the number of platforms we are trying to support (specifically console).

### Classes
| Name | Inherits | Modules | Description |
|---|---|---|---|
|	[ArgumentError](ruby/argumenterror.md)	|	[StandardError](ruby/standarderror.md)	|		|
|	[Array](ruby/array.md)	|	[Object](ruby/object.md)	|	[Enumerable](ruby/enumerable.md)	|
|	[EOFError](ruby/eoferror.md)	|	[IOError](ruby/ioerror.md)	|		|
|	[Enumerator](ruby/enumerator.md)	|	[Object](ruby/object.md)	|		|
|	[Exception](ruby/exception.md)	|	[Object](ruby/object.md)	|		|
|	[FalseClass](ruby/falseclass.md)	|	[Object](ruby/object.md)	|		|
|	[Fiber](ruby/fiber.md)	|	[Object](ruby/object.md)	|		|
|	[File](ruby/file.md)	|	[IO](ruby/io.md)	|	Constants	|
|	[FileTest](ruby/filetest.md)	|	[Object](ruby/object.md)	|		|
|	[Fixnum](ruby/fixnum.md)	|	[Integer](ruby/integer.md)	|		|
|	[Float](ruby/float.md)	|	[Numeric](ruby/numeric.md)	|		|
|	[FloatDomainError](ruby/floatdomainerror.md)	|	[RangeError](ruby/rangeerror.md)	|		|
|	[FrozenError](ruby/frozenerror.md)	|	[RuntimeError](ruby/runtimeerror.md)	|		|
|	[Hash](ruby/hash.md)	|	[Object](ruby/object.md)	|	[Enumerable](ruby/enumerable.md)	|
|	[IO](ruby/io.md)	|	[Object](ruby/object.md)	|		|
|	[IOError](ruby/ioerror.md)	|	[StandardError](ruby/standarderror.md)	|		|
|	[IndexError](ruby/indexerror.md)	|	[StandardError](ruby/standarderror.md)	|		|
|	[Integer](ruby/integer.md)	|	[Numeric](ruby/numeric.md)	|		|
|	[KeyError](ruby/keyerror.md)	|	[IndexError](ruby/indexerror.md)	|		|
|	[LocalJumpError](ruby/localjumperror.md)	|	[ScriptError](ruby/scripterror.md)	|		|
|	[Method](ruby/method.md)	|	[Object](ruby/object.md)	|		|
|	[Module](ruby/module.md)	|	[Object](ruby/object.md)	|		|
|	[NameError](ruby/nameerror.md)	|	[StandardError](ruby/standarderror.md)	|		|
|	[NilClass](ruby/nilclass.md)	|	[Object](ruby/object.md)	|	[NilClassFalseClass](ruby/nilclassfalseclass.md)	|
|	[NoMemoryError](ruby/nomemoryerror.md)	|	[Exception](ruby/exception.md)	|		|
|	[NoMethodError](ruby/nomethoderror.md)	|	[NameError](ruby/nameerror.md)	|		|
|	[NotImplementedError](ruby/notimplementederror.md)	|	[ScriptError](ruby/scripterror.md)	|		|
|	[Numeric](ruby/numeric.md)	|	[Object](ruby/object.md)	|	[Comparable](ruby/comparable.md), [ValueType](ruby/valuetype.md)	|
|	[Object](ruby/object.md)	|	[](ruby/.md)	|		|
|	[Proc](ruby/proc.md)	|	[Object](ruby/object.md)	|		|
|	[Random](ruby/random.md)	|	[Object](ruby/object.md)	|		|
|	[Range](ruby/range.md)	|	[Object](ruby/object.md)	|	[Enumerable](ruby/enumerable.md)	|
|	[RangeError](ruby/rangeerror.md)	|	[StandardError](ruby/standarderror.md)	|		|
|	[RegexpError](ruby/regexperror.md)	|	[StandardError](ruby/standarderror.md)	|		|
|	[ScriptError](ruby/scripterror.md)	|	[Exception](ruby/exception.md)	|		|
|	[StandardError](ruby/standarderror.md)	|	[Exception](ruby/exception.md)	|		|
|	[StopIterationError](ruby/stopiterationerror.md)	|	[IndexError](ruby/indexerror.md)	|		|
|	[String](ruby/string.md)	|	[Object](ruby/object.md)	|	[Comparable](ruby/comparable.md), [ValueType](ruby/valuetype.md)	|
|	[Struct](ruby/struct.md)	|	[Object](ruby/object.md)	|		|
|	[Symbol](ruby/symbol.md)	|	[Object](ruby/object.md)	|	[Comparable](ruby/comparable.md), [ValueType](ruby/valuetype.md)	|
|	[SystemStackError](ruby/systemstackerror.md)	|	[Exception](ruby/exception.md)	|		|
|	[Time](ruby/time.md)	|	[Object](ruby/object.md)	|	[Comparable](ruby/comparable.md)	|
|	[TrueClass](ruby/trueclass.md)	|	[Object](ruby/object.md)	|	[ValueType](ruby/valuetype.md)	|
|	[TypeError](ruby/typeerror.md)	|	[StandardError](ruby/standarderror.md)	|		|
|	[UnboundMethod](ruby/unboundmethod.md)	|	[Object](ruby/object.md)	|		|


### Modules
| Name | Description |
|---|---|
|	[BasicObject](ruby/basicobject.md)	|		|
|	[Comparable](ruby/comparable.md)	|		|
|	[Enumerable](ruby/enumerable.md)	|		|
|	[Kernel](ruby/kernel.md)	|		|
|	[Math](ruby/math.md)	|		|
|	[NilClassFalseClass](ruby/nilclassfalseclass.md)	|		|
|	[ValueType](ruby/valuetype.md)	|		|



