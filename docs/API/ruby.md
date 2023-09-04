  <script type="module">
    import mermaid from "https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs";
    mermaid.initialize({ startOnLoad: true });
    window.mermaid = mermaid;
  </script>
  <script src="//unpkg.com/docsify-mermaid@2.0.0/dist/docsify-mermaid.js"></script>

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

class Array {
~Enumerable
}

class Enumerator {
~Enumerable
}

class Chain {
~Enumerable
}

class Generator {
~Enumerable
}
class Range {
~Enumerable
}

class File {
~Constants
}

class Socket {
~Constants
~Option
}

class Integer {
~Integral
}

class Numeric {
~Comparable
}

class String {
~Comparable
}

class Symbol {
~Comparable
}
```
