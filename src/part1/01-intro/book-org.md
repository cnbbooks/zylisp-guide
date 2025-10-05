# Book Organisation

This book is organised to take you from your first steps with Zylisp through to advanced metaprogramming and performance optimisation. Whether you're coming from Go, another Lisp dialect, or learning your first systems programming language, the structure guides you through increasingly sophisticated concepts while building on what you've already learnt.

## Part I: Getting Started with Zylisp

We begin with the essentials. After exploring why Zylisp exists and its fascinating heritage—drawing from ZetaLisp, Erlang, Clojure, LFE, and Go—you'll write your first programme, learn to use the REPL, and set up your development environment. A guided tour then introduces you to real-world Zylisp through complete working examples: parsing command-line arguments, building a web server, and implementing concurrent URL fetching. These examples demonstrate the language's philosophy before we dive into the details.

## Part II: Zylisp Fundamentals

Here you'll master the core language. We cover programme structure, from s-expressions to packages; basic data types including numbers, strings, and booleans; and functions in depth—declarations, recursion, closures, and error handling. This part establishes the foundation for everything that follows.

## Part III: Immutable Data Structures

Zylisp's commitment to immutability by default sets it apart from traditional Lisps and Go alike. This part explores lists, vectors, maps, sets, and records, explaining not just how to use them but how structural sharing makes immutability efficient. Pattern matching—one of Zylisp's most powerful features—gets its own chapter, covering everything from basic destructuring to advanced patterns with guards.

## Part IV: Types and Abstraction

Moving beyond basics, we explore Zylisp's type system: annotations, inference, parametric polymorphism, and the relationship between type aliases and new types. You'll learn to define structs and records, work with methods, and understand how embedding enables composition. These chapters show how Zylisp brings type safety to Lisp whilst maintaining expressiveness.

## Part V: Interfaces and Protocols

Interfaces enable polymorphism and abstraction in Zylisp. We cover interface contracts, satisfaction, type assertions and switches, and composition. A separate chapter on common interfaces—for string conversion, errors, comparison, iteration, and I/O—provides practical patterns you'll use constantly.

## Part VI: Concurrency (The Go Way in Lisp)

Zylisp inherits Go's elegant concurrency model. These chapters explain goroutines, channels (buffered and unbuffered), and essential concurrency patterns: select expressions, timeouts, pipelines, fan-out/fan-in, and cancellation. We also cover synchronisation primitives and show how immutability itself serves as a synchronisation mechanism.

## Part VII: Organising Code

As your programmes grow, organisation matters. This part covers modules and packages, testing (including property-based testing), and documentation. You'll learn Zylisp's conventions for structuring larger projects and maintaining them over time.

## Part VIII: Advanced Features

Now we reach what makes Lisp special: macros and metaprogramming. You'll learn to write macros hygienically, understand quoting and unquoting, and recognise when macros are the right tool. Chapters on compile-time evaluation, reader macros, and building domain-specific languages show how Zylisp extends itself. Reflection rounds out this part, though we emphasise when *not* to use these powerful features.

## Part IX: Interoperability and Performance

The final part addresses practical concerns. Zylisp's Go interoperability means you can call Go functions, use Go packages, and even integrate with C through CGo. We cover profiling, memory management, optimisation techniques, and when to drop to Go for performance. A chapter on unsafe operations explains the escape hatches available when you need them.

## Appendices

Six appendices provide reference material: complete syntax grammar, standard library overview, pattern matching reference, type system reference, and comparison guides for readers coming from other Lisps or from Go. These serve as quick references long after you've finished reading.

## How to Read This Book

If you're new to both Lisp and systems programming, read sequentially—each part builds on previous ones. Experienced Lispers might skim Part II and focus on Parts IV, VI, and VIII to understand Zylisp's type system, concurrency model, and macro hygiene. Go programmers should read Part I, then jump to Parts III and VIII to understand immutability and macros before circling back to fill gaps.

Code examples are complete and runnable. Type them in, experiment with variations, and make predictions about behaviour before running them. The REPL makes exploration natural—use it liberally.

Most importantly, Zylisp rewards a certain mindset: think in immutable transformations, embrace pattern matching, and use macros sparingly but powerfully. This book aims to cultivate that mindset alongside teaching the mechanics of the language.
