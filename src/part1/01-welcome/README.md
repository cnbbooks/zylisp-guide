# Welcome to Zylisp

Zylisp is a Lisp dialect that brings together two seemingly disparate programming traditions: the expressive, homoiconic power of Lisp and the pragmatic, concurrent design of Go. It is a language for building reliable, concurrent systems while maintaining the flexibility and metaprogramming capabilities that have made Lisp enduringly relevant for over six decades.

At its core, Zylisp embraces immutability by default. Data structures are persistent and immutable, enabling fearless concurrent programming without sacrificing the elegance of functional composition. Yet when performance demands it, the language provides well-defined escape hatches through its unsafe package and mutable operations. This design philosophy extends throughout: strong opinions with practical exits.

Concurrency in Zylisp follows Go's CSP-inspired model. Goroutines and channels are first-class constructs, expressed in Lisp's parenthetical syntax. The result is concurrent code that is both highly readable and compositionally powerful—pipeline architectures that can be built, reasoned about, and refactored with the full toolkit of functional programming. Combined with Zylisp's immutable-by-default data structures, concurrent programs gain an additional layer of safety that even Go cannot provide.

The type system is optional but pervasive. Type annotations guide the compiler where precision matters; type inference fills in the gaps. Pattern matching—a feature conspicuously absent from Go—becomes a primary means of destructuring data and controlling program flow. And because Zylisp is a Lisp, code is data and data is code: macros provide compile-time metaprogramming that can extend the language itself.

Zylisp does not abandon the pragmatism that makes Go successful. Direct interoperability with Go packages means access to Go's rich ecosystem. The compilation model targets Go's runtime, inheriting its garbage collector, scheduler, and cross-platform build tooling. Zylisp programs can call Go functions; Go programs can embed Zylisp.

This guide assumes you have programmed before, whether in Lisp, Go, or other languages. If you come from the Lisp tradition, you will recognize the s-expressions, the macros, and the functional style—but discover Go's concurrency primitives and struct-based object model. If you come from Go, you will recognize goroutines, channels, and interfaces—but discover pattern matching, immutable data structures, and compile-time metaprogramming. And if you come from elsewhere, you may find Zylisp a compelling synthesis of ideas that have each proven valuable in isolation.

Let us begin.
