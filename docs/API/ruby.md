# Classes
| Name | Inherits | Includes | Description |
|---|---|---|---|
| Hash | Object | Enumerable | Associative Array |

# Modules
| Name | Description |
|---|---|
| Enumerable | |

# Inheritance Diagram
```mermaid
classDiagram
Object<|--Hash
Object<|--Array
Object<|--AddrInfo
Object<|--Enumerator
Object<|--Chain
Object<|--Generator
Object<|--Yielder
Object<|--FalseClass
Object<|--Fiber
Object<|--Exception
Object<|--FileTest
Object<|--IO
Object<|--Method
Object<|--Module
Object<|--NilClass
Object<|--Numeric
Object<|--Proc
Object<|--Random
Object<|--Range
Object<|--String
Object<|--Struct
Object<|--Symbol
Object<|--Time
Object<|--TrueClass
Object<|--UnboundMethod


Enumerator<|--Lazy

IO<|--BasicSocket
IO<|--File
BasicSocket<|--IPSocket
BasicSocket<|--Socket
BasicSocket<|--UNIXSocket
UNIXSocket<|--UNIXServer
IPSocket<|--TCPSocket
IPSocket<|--UDPSocket
TCPSocket<|--TCPServer


Integer<|--Fixnum
Numeric<|--Complex
Numeric<|--Float
Numeric<|--Integer
Numeric<|--Rational

Exception<|--NoMemoryError
Exception<|--ScriptError
Exception<|--StandardError
Exception<|--SystemStackError


IOError<|--EOFError
StandardError<|--ArgumentError
StandardError<|--IOError
StandardError<|--IndexError
StandardError<|--NameError
StandardError<|--RangeError
StandardError<|--RegexpError
StandardError<|--SocketError
StandardError<|--TypeError
NameError<|--NoMethodError
IndexError<|--KeyError
IndexError<|--StopIteration
RangeError<|--FloatDomainError
RuntimeError<|--FrozenError
ScriptError<|--LocalJumpError
ScriptError<|--NotImplementedError



class Hash {
~Enumerable
}
```
