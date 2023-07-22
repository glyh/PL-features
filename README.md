[Rationale](https://github.com/glyh/nontrivial-PL-features/blob/main/rationale.md) [Convention](https://github.com/glyh/nontrivial-PL-features/blob/main/convention.md) [Contributing](https://github.com/glyh/nontrivial-PL-features/blob/main/contributing.md)

## List of features

#### [Async/await](https://en.wikipedia.org/wiki/Async/await)
  - Description: A syntax sugar for writing [asynchronous](https://en.wikipedia.org/wiki/Async/await) [concurrent](https://en.wikipedia.org/wiki/Concurrency_(computer_science)) code that looks serial.
  - Implementation: [Javascript](https://www.javascript.com/) [async-await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)
  - Pros: Readability
  - Cons: Uncontrolable

#### Caching with Reactive Invalidation
  - Description: Caching the result of function, invalidating the data reactively when the cache are potentially outdated.
  - Implementation: [Skip](http://skiplang.com/docs/tutorial.html) [Caching with reactive invalidation](http://skiplang.com/)
  - Pros:
    - User doesn't have to invalidate cache on their own

#### Comptime
  - Description: Evaluation of code at [compile time](https://en.wikipedia.org/wiki/Compile_time) and compile-time [duck-typing](https://en.wikipedia.org/wiki/Duck_typing).
  - Implementation: [Zig](https://ziglang.org/) [comptime](https://ziglang.org/documentation/master/#comptime)
  - Pros: 
    - Eliminate the need of generics: generics are just compile time evaluated function from types to types
  - Cons: Compilation speed

#### Coroutine 
  - Description: A syntax sugar for structuring [cooperative](https://en.wikipedia.org/wiki/Cooperative_multitasking) [concurrent](https://en.wikipedia.org/wiki/Concurrency_(computer_science)) code modularly.
  - Implementation: [Lua](https://www.lua.org/) [coroutine](https://www.lua.org/pil/9.1.html)
  - Pros: Readablility

#### Effect System
  - Description: A system similar to type system, but tracks side effects instead of type of the value.
  - Implementation: (koka)[https://koka-lang.github.io/koka/doc/index.html] [effect system](https://en.wikipedia.org/wiki/Effect_system)

#### Garbage Collection
  - Description: A system that free unused [heap-allocated](https://en.wikipedia.org/wiki/C_dynamic_memory_allocation) memory in [runtime](https://en.wikipedia.org/wiki/Runtime_system)
  - Implementation: [Common Lisp](https://lisp-lang.org/) [GC](https://en.wikipedia.org/wiki/Garbage_collection_(computer_science))
  - Pros: Developer-friendliness
  - Cons: Performance

#### Green Threads
  - Description: An abstraction that allow easily writing [preemptive](https://en.wikipedia.org/wiki/Preemption_(computing)) [concurrent](https://en.wikipedia.org/wiki/Concurrency_(computer_science)) code, without actually using OS thread
  - Implementation: [Java](https://www.java.com/) [green threads](https://en.wikipedia.org/wiki/Green_thread)
  - Pros: 
    - potential performance boost by not wasting time on OS context switch.

#### Hygienic Macros
  - Description: Lisp macros that follows [lexical scope](https://en.wikipedia.org/wiki/Scope_(computer_science)#Lexical_scope).
  - Implementation: [Scheme](https://www.scheme.com/) [Hygienic macro](https://docs.scheme.org/guide/macros/)
  - Based-on: [Lisp Macros](1https://github.com/glyh/nontrivial-PL-features#lisp-macros)
  - Pros: Debuggablility 

#### Lazy Evaluation
  - Description: Any portion of the code is evaluated only when needed.
  - Implementation: [Haskell](https://www.haskell.org/) [lazy evaluation](https://wiki.haskell.org/Lazy_evaluation)
  - Pros: 
    - Easy to implement infinite data structures
    - Potential performance boost by not evaluating unnecessary code
  - Cons: Undebuggable

#### Lisp Macros
  - Description: [Compile-time](https://en.wikipedia.org/wiki/Compile_time) [AST](https://en.wikipedia.org/wiki/Abstract_syntax_tree)-based code generation in a [homoiconic](https://en.wikipedia.org/wiki/Homoiconicity) and [dynamically-typed](https://en.wikipedia.org/wiki/Type_system#Dynamic_type_checking_and_runtime_type_information) language.
  - Implementation: [Common Lisp](https://lisp-lang.org/) [macros](https://lispcookbook.github.io/cl-cookbook/macros.html)
  - Pros: DRY, Productibility
  - Cons: Debuggablility, Readablility, Performance Predictablity

#### Ownership
  - Description: A system that helps compiler decide when to free [heap-allocated memory](https://en.wikipedia.org/wiki/C_dynamic_memory_allocation) statically.
  - Implementation: [Rust](https://www.rust-lang.org/) [Ownership](https://doc.rust-lang.org/book/ch04-00-understanding-ownership.html)
  - Pros: Performance
  - Cons: Readablility, Developer-friendliness 

#### Pattern matching 
  - Description: A structural way for obtain data from complicated [data structures](https://en.wikipedia.org/wiki/Data_structure).
  - Implementation: [Haskell](https://www.haskell.org/) [pattern matching](https://www.haskell.org/tutorial/patterns.html)
  - Pros: Readablility, Optimizabililty

#### Row Polymorphism
  - Description: A polymorphism that dispatch on concerned record fields and their type.
  - Implementation: [OCaml](https://ocaml.org/) [row polymorphism](https://www.cl.cam.ac.uk/teaching/1415/L28/rows.pdf)
  - Pros: 
    - Flexibility compared to subtyping

#### [Universal Function Call Syntax](https://en.wikipedia.org/wiki/Uniform_Function_Call_Syntax)
  - Description: A syntax sugar for function call that makes chaining function calls easy.
  - Implementation: [Nim](https://nim-lang.org/) [UFCS](https://narimiran.github.io/nim-basics/#_calling_the_procedures), [Elixir](https://elixir-lang.org/) [Pipe Operator](https://elixir-lang.org/getting-started/enumerables-and-streams.html#the-pipe-operator), [Clojure](https://clojure.org/) [Threading Macro](https://clojure.org/guides/threading_macros)
  - Pros: Readablility
