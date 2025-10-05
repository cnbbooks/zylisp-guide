[The Zylisp Guide](README.md)
[Title Page](fm/title-page.md)
[Copyright](fm/copyright.md)
[About the Cover](fm/about-cover.md)

---

[Dedication](preface/dedication.md)
[Preface](preface/README.md)
[Forward](preface/forward.md)
[Acknowledgments](preface/acknowledgments.md)

---

# Part I: Getting Started with Zylisp

- [Introduction](./part1/01-intro/README.md)
  - [Why Zylisp?](./part1/01-intro/why-zylisp.md)
  - [Origins](./part1/01-intro/origins.md)
  - [The Zylisp Project](./part1/01-intro/the-project.md)
  - [Book Organisation](./part1/01-intro/book-org.md)

- [Welcome to Zylisp](./part1/02-welcome/README.md)
  - [Hello, World](./part1/02-welcome/hello-world.md)
  - [The REPL](./part1/02-welcome/the-repl.md)
  - [Setting Up Your Environment](./part1/02-welcome/env-setup.md)

- [A Tour of Zylisp](./part1/03-tour/README.md)
  - [Command-Line Arguments](./part1/03-tour/cli-args.md)
  - [Finding Duplicate Lines](./part1/03-tour/finding-duplicate-lines.md)
  - [A Web Server](./part1/03-tour/web-server.md)
  - [Concurrent URL Fetching](./part1/03-tour/concurrent-web.md)
  - [Loose Ends](./part1/03-tour/loose-ends.md)

---

# Part II: Zylisp Fundamentals

- [Program Structure](./part2/04-prog-structr/README.md)
  - [Expressions and S-Expressions](./part2/04-prog-structr/expr-sexpr.md)
  - [Definitions and Declarations](./part2/04-prog-structr/def-dec.md)
  - [Names and Naming Conventions](./part2/04-prog-structr/names-conv.md)
  - [Scope and Visibility](./part2/04-prog-structr/scope-vis.md)
  - [Packages and Files](./part2/04-prog-structr/pack-file.md)
  - [Comments and Documentation](./part2/04-prog-structr/com-doc.md)

- [Basic Data Types](./part2/05-basic-types/README.md)
  - [Numbers](./part2/05-basic-types/nums.md)
  - [Booleans](./part2/05-basic-types/bools.md)
  - [Strings and Runes](./part2/05-basic-types/strs-rns.md)
  - [Constants](./part2/05-basic-types/consts.md)
  - [Type Declarations](./part2/05-basic-types/types.md)

- [Functions](./part2/06-funcs/README.md)
  - [Function Declarations](./part2/06-funcs/func-dec.md)
  - [Parameters and Arguments](./part2/06-funcs/param-args.md)
  - [Multiple Return Values](./part2/06-funcs/return-vals.md)
  - [Recursion](./part2/06-funcs/recurs.md)
  - [Anonymous Functions and Closures](./part2/06-funcs/lambda.md)
  - [Variadic Functions](./part2/06-funcs/variadic-funcs.md)
  - [Higher-Order Functions](./part2/06-funcs/higher-order-funcs.md)
  - [Error Handling](./part2/06-funcs/errs.md)

---

# Part III: Immutable Data Structures

- [Lists and Sequences](./part3/07-lists/README.md)
  - [The List: Lisp's Fundamental Structure](./part3/07-lists/the-list.md)
  - [List Operations](./part3/07-lists/list-ops.md)
  - [Immutability Guarantees](./part3/07-lists/immut-guar.md)
  - [Sharing and Structural Sharing](./part3/07-lists/struct-share.md)
  - [List Comprehensions](./part3/07-lists/list-comp.md)

- [Composite Types](./part3/08-comp-types/README.md)
  - [Vectors (Immutable Arrays)](./part3/08-comp-types/vecs.md)
  - [Maps (Immutable Hash Tables)](./part3/08-comp-types/maps.md)
  - [Sets](./part3/08-comp-types/sets.md)
  - [Records](./part3/08-comp-types/recs.md)
  - [Working with Immutable Data](./part3/08-comp-types/immut-data.md)

- [Pattern Matching](./part3/09-pat-match/README.md)
  - [Introduction to Pattern Matching](./part3/09-pat-match/intro.md)
  - [Basic Patterns](./part3/09-pat-match/basic-pats.md)
  - [Destructuring](./part3/09-pat-match/destruct.md)
  - [Guards and Conditionals](./part3/09-pat-match/guards.md)
  - [Pattern Matching in Function Parameters](./part3/09-pat-match/func-params.md)
  - [Advanced Patterns](./part3/09-pat-match/adv-pats.md)
  - [Implementation Notes](./part3/09-pat-match/impl-notes.md)

---

# Part IV: Types and Abstraction

- [The Type System](./part4/10-types/README.md)
  - [Type Annotations](./part4/10-types/type-annot.md)
  - [Type Inference](./part4/10-types/type-infer.md)
  - [Basic Type Checking](./part4/10-types/type-check.md)
  - [Function Types](./part4/10-types/func-types.md)
  - [Parametric Polymorphism](./part4/10-types/poly.md)
  - [Type Aliases vs New Types](./part4/10-types/aliases.md)
  - [The Unit Type and Void](./part4/10-types/unit-void.md)

- [Structs and Records](./part4/11-structs/README.md)
  - [Defining Structs](./part4/11-structs/def-structs.md)
  - [Field Access and Updates](./part4/11-structs/field-access.md)
  - [Struct Embedding](./part4/11-structs/embed.md)
  - [Struct Patterns in Matching](./part4/11-structs/pats.md)
  - [Immutable Structs by Default](./part4/11-structs/immut.md)

- [Methods](./part4/12-methods/README.md)
  - [Method Declarations](./part4/12-methods/method-dec.md)
  - [Receiver Types](./part4/12-methods/recv-types.md)
  - [Value Receivers](./part4/12-methods/val-recv.md)
  - [Method Sets](./part4/12-methods/method-sets.md)
  - [Composing Types with Embedding](./part4/12-methods/compose.md)
  - [Encapsulation](./part4/12-methods/encap.md)

---

# Part V: Interfaces and Protocols

- [Interfaces](./part5/13-ifaces/README.md)
  - [Interfaces as Contracts](./part5/13-ifaces/contracts.md)
  - [Defining Interfaces](./part5/13-ifaces/def-ifaces.md)
  - [Interface Satisfaction](./part5/13-ifaces/satisf.md)
  - [The Empty Interface](./part5/13-ifaces/empty-iface.md)
  - [Type Assertions](./part5/13-ifaces/type-assert.md)
  - [Type Switches](./part5/13-ifaces/type-switch.md)
  - [Interface Composition](./part5/13-ifaces/compose.md)

- [Common Interfaces](./part5/14-com-ifaces/README.md)
  - [String Conversion](./part5/14-com-ifaces/str-conv.md)
  - [Error Handling Interface](./part5/14-com-ifaces/err-iface.md)
  - [Comparison and Ordering](./part5/14-com-ifaces/comp-order.md)
  - [Iteration Protocols](./part5/14-com-ifaces/iter.md)
  - [I/O Interfaces](./part5/14-com-ifaces/io.md)

---

# Part VI: Concurrency (The Go Way in Lisp)

- [Goroutines](./part6/15-gotines/README.md)
  - [What Are Goroutines?](./part6/15-gotines/what-are.md)
  - [Creating Goroutines](./part6/15-gotines/creating.md)
  - [Goroutine Lifecycle](./part6/15-gotines/lifecycle.md)
  - [Goroutines vs OS Threads](./part6/15-gotines/vs-threads.md)
  - [Example: Concurrent Server](./part6/15-gotines/example.md)

- [Channels](./part6/16-chans/README.md)
  - [Channel Basics](./part6/16-chans/basics.md)
  - [Creating Channels](./part6/16-chans/creating.md)
  - [Sending and Receiving](./part6/16-chans/send-recv.md)
  - [Buffered vs Unbuffered Channels](./part6/16-chans/buffered.md)
  - [Channel Direction](./part6/16-chans/direction.md)
  - [Closing Channels](./part6/16-chans/closing.md)
  - [Range over Channels](./part6/16-chans/range.md)

- [Concurrency Patterns](./part6/17-conc-pats/README.md)
  - [Select Expression](./part6/17-conc-pats/select.md)
  - [Timeouts](./part6/17-conc-pats/timeouts.md)
  - [Non-Blocking Operations](./part6/17-conc-pats/non-blocking.md)
  - [Pipelines](./part6/17-conc-pats/pipelines.md)
  - [Fan-Out, Fan-In](./part6/17-conc-pats/fan.md)
  - [Cancellation](./part6/17-conc-pats/cancel.md)
  - [Context](./part6/17-conc-pats/context.md)

- [Synchronization](./part6/18-sync/README.md)
  - [When to Use Synchronization](./part6/18-sync/when.md)
  - [Mutexes](./part6/18-sync/mutexes.md)
  - [Read-Write Locks](./part6/18-sync/rw-locks.md)
  - [Atomic Operations](./part6/18-sync/atomic.md)
  - [The Race Detector](./part6/18-sync/race-detect.md)
  - [Immutability as Synchronization](./part6/18-sync/immut-sync.md)

---

# Part VII: Organizing Code

- [Modules and Packages](./part7/19-mods/README.md)
  - [Package Structure](./part7/19-mods/pack-struct.md)
  - [Import Declarations](./part7/19-mods/imports.md)
  - [Export and Visibility](./part7/19-mods/export-vis.md)
  - [Package Initialization](./part7/19-mods/init.md)
  - [Internal Packages](./part7/19-mods/internal.md)
  - [Versioning and Dependencies](./part7/19-mods/versions.md)

- [Testing](./part7/20-testing/README.md)
  - [Writing Tests](./part7/20-testing/writing.md)
  - [Running Tests](./part7/20-testing/running.md)
  - [Test Coverage](./part7/20-testing/coverage.md)
  - [Benchmarks](./part7/20-testing/benchmarks.md)
  - [Example Functions](./part7/20-testing/examples.md)
  - [Property-Based Testing](./part7/20-testing/prop-based.md)

- [Documentation](./part7/21-docs/README.md)
  - [Doc Comments](./part7/21-docs/doc-comments.md)
  - [Generating Documentation](./part7/21-docs/gen-docs.md)
  - [Examples in Documentation](./part7/21-docs/examples.md)
  - [Package Documentation](./part7/21-docs/pack-docs.md)

---

# Part VIII: Advanced Features

- [Macros](./part8/22-macros/README.md)
  - [What Are Macros?](./part8/22-macros/what-are.md)
  - [Defining Macros](./part8/22-macros/defining.md)
  - [Quoting and Unquoting](./part8/22-macros/quote-unquote.md)
  - [Hygiene and Symbol Capture](./part8/22-macros/hygiene.md)
  - [Common Macro Patterns](./part8/22-macros/patterns.md)
  - [When to Use Macros](./part8/22-macros/when.md)
  - [Macro Debugging](./part8/22-macros/debugging.md)

- [More Metaprogramming](./part8/23-metaprog/README.md)
  - [Code as Data, Data as Code](./part8/23-metaprog/code-as-data.md)
  - [Compile-Time Evaluation](./part8/23-metaprog/compile-time.md)
  - [Reader Macros](./part8/23-metaprog/reader-macros.md)
  - [Syntax Objects](./part8/23-metaprog/syntax-objs.md)
  - [Building DSLs](./part8/23-metaprog/dsls.md)

- [Reflection](./part8/24-refl/README.md)
  - [Type Reflection](./part8/24-refl/type-refl.md)
  - [Value Inspection](./part8/24-refl/val-inspect.md)
  - [Struct Tags](./part8/24-refl/tags.md)
  - [Dynamic Invocation](./part8/24-refl/dyn-invoke.md)
  - [When to Use Reflection](./part8/24-refl/when.md)

---

# Part IX: Interoperability and Performance

- [Go Interoperability](./part9/25-go-interop/README.md)
  - [Calling Go Functions](./part9/25-go-interop/calling.md)
  - [Using Go Packages](./part9/25-go-interop/packages.md)
  - [Wrapping Go Types](./part9/25-go-interop/wrapping.md)
  - [CGo Integration](./part9/25-go-interop/cgo.md)
  - [Performance Considerations](./part9/25-go-interop/perf.md)

- [Performance](./part9/26-perf/README.md)
  - [Profiling Zylisp Programs](./part9/26-perf/profiling.md)
  - [Memory Management](./part9/26-perf/memory.md)
  - [Immutable Data Performance](./part9/26-perf/immut-perf.md)
  - [Optimization Techniques](./part9/26-perf/optim.md)
  - [When to Drop to Go](./part9/26-perf/drop-to-go.md)

- [Unsafe Operations](./part9/27-unsafe/README.md)
  - [The unsafe Package](./part9/27-unsafe/package.md)
  - [Mutable Operations](./part9/27-unsafe/mutable.md)
  - [Raw Pointers](./part9/27-unsafe/pointers.md)
  - [When Unsafe is Justified](./part9/27-unsafe/when.md)

---

# Appendices

- [Appendix I: Syntax Reference](./appendices/i/syntax-ref/README.md)
  - [S-Expression Grammar](./appendices/i/syntax-ref/sexpr-grammar.md)
  - [Special Forms](./appendices/i/syntax-ref/specl-forms.md)
  - [Built-in Functions](./appendices/i/syntax-ref/built-in-funcs.md)
  - [Reserved Words](./appendices/i/syntax-ref/res-words.md)

- [Appendix II: Standard Library Overview](./appendices/ii/stdlib-overview/README.md)
  - [Core Functions](./appendices/ii/stdlib-overview/core-funcs.md)
  - [Data Structure Libraries](./appendices/ii/stdlib-overview/struct-libs.md)
  - [I/O and File System](./appendices/ii/stdlib-overview/io-fs.md)
  - [Networking](./appendices/ii/stdlib-overview/net.md)
  - [Concurrency Utilities](./appendices/ii/stdlib-overview/concurr.md)
  - [Testing Utilities](./appendices/ii/stdlib-overview/testing.md)

- [Appendix III: Pattern Matching Reference](./appendices/iii/pat-match-ref/README.md)
  - [Pattern Syntax](./appendices/iii/pat-match-ref/pat-syntax.md)
  - [Pattern Types](./appendices/iii/pat-match-ref/pat-types.md)
  - [Match Expression Forms](./appendices/iii/pat-match-ref/match-expr.md)
  - [Implementation Details](./appendices/iii/pat-match-ref/impl-deets.md)

- [Appendix IV: Type System Reference](./appendices/iv/types-ref/README.md)
  - [Type Syntax](./appendices/iv/types-ref/syntax.md)
  - [Type Inference Rules](./appendices/iv/types-ref/infer.md)
  - [Subtyping Relations](./appendices/iv/types-ref/subtype-rels.md)
  - [Generic Type Parameters](./appendices/iv/types-ref/generic-params.md)

- [Appendix V: Comparison with Other Lisps](./appendices/v/lisp-comp/README.md)
  - [From Common Lisp](./appendices/v/lisp-comp/common-lisp.md)
  - [From Scheme/Racket](./appendices/v/lisp-comp/racket.md)
  - [From Clojure](./appendices/v/lisp-comp/clojure.md)
  - [From LFE](./appendices/v/lisp-comp/lfe.md)

- [Appendix VI: Comparison with Go](./appendices/v/go-comp/README.md)
  - [Syntax Mapping](./appendices/vi/go-comp/syntax-map.md)
  - [Idiom Translation](./appendices/vi/go-comp/idioms.md)
  - [What's Different](./appendices/vi/go-comp/diff.md)
  - [What's the Same](./appendices/vi/go-comp/same.md)
