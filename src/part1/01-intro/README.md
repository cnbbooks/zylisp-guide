# Introduction

Zylisp is a modern Lisp dialect that compiles to Go, bringing together two seemingly disparate programming traditions: the expressive, homoiconic power of Lisp and the pragmatic, concurrent design of Go. It unites Lisp's metaprogramming capabilities with contemporary language features—static typing with inference, immutability by default, sophisticated pattern matching, and Go's proven concurrency model—creating a language for building reliable, concurrent systems whilst maintaining the flexibility that has made Lisp enduringly relevant for over six decades.

At its core, Zylisp embraces immutability by default. Data structures are persistent and immutable, enabling fearless concurrent programming without sacrificing the elegance of functional composition. Yet when performance demands it, the language provides well-defined escape hatches through its unsafe package and mutable operations. This design philosophy extends throughout: strong opinions with practical exits.

Concurrency in Zylisp follows Go's CSP-inspired model. Goroutines and channels are first-class constructs, expressed in Lisp's parenthetical syntax. The result is concurrent code that is both highly readable and compositionally powerful—pipeline architectures that can be built, reasoned about, and refactored with the full toolkit of functional programming. Combined with Zylisp's immutable-by-default data structures, concurrent programs gain an additional layer of safety that even Go cannot provide.

The type system is optional but pervasive. Type annotations guide the compiler where precision matters; type inference fills in the gaps. Pattern matching—a feature conspicuously absent from Go—becomes a primary means of destructuring data and controlling program flow. And because Zylisp is a Lisp, code is data and data is code: macros provide compile-time metaprogramming that can extend the language itself.

Zylisp does not abandon the pragmatism that makes Go successful. Direct interoperability with Go packages means access to Go's rich ecosystem. The compilation model targets Go's runtime, inheriting its garbage collector, scheduler, and cross-platform build tooling. Zylisp programs can call Go functions; Go programs can embed Zylisp.

## General Goals

### Primary Objectives

**1. Lisp Heritage with Modern Sensibilities**

- Full macro system with hygiene and phase separation
- Code-as-data philosophy (homoiconicity)
- S-expression syntax as the primary interface
- Ability to build domain-specific languages

**2. Type Safety Without Ceremony**

- Static type system with powerful inference
- Parametric polymorphism (generics)
- Gradual typing where appropriate
- Type annotations as documentation and verification

**3. Immutability Good Citizenship**

- Persistent data structures when possible
- Structural sharing for performance
- Explicit opt-in for mutation when needed
- Safe concurrent access without locks

**4. Go's Concurrency Model**

- Native goroutines and channels
- CSP-style concurrent programming
- Supervision trees for fault tolerance (Erlang-inspired)
- Combined management of OS processes and goroutines

**5. Seamless Go Interoperability**

- Compile to readable, idiomatic Go source code
- Call Go functions and use Go packages directly
- Access to the entire Go ecosystem
- Integration with Go's tooling and build system

**6. Production-Ready Systems Language**

- Not merely a research project or toy language
- Focus on practical, real-world applications
- Performance comparable to hand-written Go
- Comprehensive error reporting and debugging support

### Philosophical Position

Zylisp occupies a unique niche by combining:

- **Erlang's** supervision trees, fault-tolerant system design, and data immutability
- **Clojure's** immutable-by-default philosophy, persistent data structures, and deeply consistent standard library
- **Go's** pragmatic type system, concurrency primitives, and tooling
- **Common Lisp's** powerful macro system and REPL-driven development
- **Scheme's** elegance and minimalist core

The result is a language suitable for building reliable, concurrent systems whilst maintaining the interactive, exploratory development style that makes Lisp productive.
