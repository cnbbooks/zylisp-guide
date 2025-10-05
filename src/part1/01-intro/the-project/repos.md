# Code Repositories

## Core Language Repositories

### **zylisp/design**

*Language research, design documents, and proposals*

**Purpose:** The intellectual foundation and specification of Zylisp.

**Contents:**

- Language design documents (30+ proposals as of October 2025)
- Architecture decisions and rationales
- Feature specifications and RFCs
- Research into complex implementation challenges
- Comparative analysis with other languages

**Key Design Documents:**

- **0001** - Go-Lisp: A Letter of Intent (the founding vision)
- **0002** - Architecture & Project Structure
- **0019** - Complete System Design
- **0024** - Error Handling Design
- **0025** - Pattern Matching Compilation
- **0027** - Forms & Expansion Pipeline
- **0030** - Erlang-Style Supervision

**Why it matters:** This repository ensures that design decisions are deliberate, documented, and debated before implementation. It serves as the "constitution" of Zylisp, explaining not just *what* the language does, but *why* it does it that way.

---

### **zylisp/lang**

*Core language implementation*

**Purpose:** The heart of Zylisp - what makes it "Lisp".

- S-expression evaluation engine
- Macro system implementation
- Macro expansion pipeline
- Special forms and core language constructs
- Built-in functions and operations
- Language semantics and evaluation rules

**Relationship to other repos:**

- Consumes source code and produces expanded forms
- Transforms Zylisp-specific constructs into ZAST
- Uses `core` for source position tracking
- Depends on `runtime` for persistent data structures

**Why it matters:** This defines the Zylisp language itself. Everything that makes Zylisp different from "Go with parentheses" lives here: macros, homoiconicity, the evaluation model, and Lisp-specific features.

---

### **zylisp/zast**

*Zylisp's Intermediate Representation - S-expressions of the Go AST*

**Purpose:** The crucial translation layer between Lisp and Go.

- S-expression representation of every Go AST node type
- IR (Intermediate Representation) transformations
- AST construction and manipulation utilities
- Canonical forms for Go constructs (see Design Doc 0003)
- Round-trip conversion: Go AST ↔ S-expressions

**Key innovation:** ZAST allows Lisp code to cleanly map to Go constructs whilst maintaining homoiconic properties. It's "Go AST with parentheses" - you can manipulate Go code structure using Lisp techniques.

**Example:**

```lisp
;; This ZAST:
(FuncDecl "factorial"
  (FieldList (Field "n" "int"))
  (FieldList (Field "" "int"))
  (BlockStmt ...))

;; Represents this Go:
func factorial(n int) int { ... }
```

**Relationship to other repos:**

- Receives macro-expanded code from `lang`
- Verified for completeness by `go-ast-coverage`
- Used by compiler to generate final Go source

**Why it matters:** This is the bridge that makes the entire project possible. By representing Go's AST as s-expressions, Zylisp can generate any valid Go construct whilst allowing Lisp-style code manipulation.

---

## Development Tools

### **zylisp/cli**

*Command-line interface and tools*

**Purpose:** User-facing entry point to the Zylisp ecosystem.

- `zylisp` binary - starts REPL servers and clients
- `zyc` binary - the Zylisp compiler
- Command-line argument parsing
- Tool orchestration and workflow management
- Configuration file handling

**User workflows:**

```bash
# Start a REPL for interactive development
zylisp repl

# Compile a Zylisp file to Go
zyc compile myfile.zy

# Run tests
zyc test ./...

# Build an executable
zyc build -o myapp
```

**Why it matters:** This is how developers interact with Zylisp day-to-day. Good CLI design makes the language accessible and productive.

---

### **zylisp/repl**

*Interactive development environment*

**Purpose:** The Read-Eval-Print-Loop, central to Lisp development.

- REPL server implementation
- REPL client implementation
- Interactive evaluation and debugging
- Code completion and introspection
- Help systems and documentation lookup
- Multi-client support (see Design Docs 0013, 0014)

**Architecture highlights:**

- Client-server design for flexibility
- Memory management and resource cleanup
- Process supervision for stability
- Support for remote REPLs
- Integration with editors and IDEs

**Why it matters:** The REPL is not an afterthought in Lisp - it's the primary development interface. Zylisp's REPL architecture enables sophisticated interactive development whilst managing resources carefully.

---

## Runtime and Support

### **zylisp/runtime**

*Shared runtime code for generated Go programs*

**Purpose:** Infrastructure that compiled Zylisp programs depend on.

- Persistent data structure implementations (lists, vectors, maps, sets)
- Structural sharing mechanisms for efficiency
- Core runtime functions
- Type system runtime support
- Pattern matching runtime helpers
- Channel and concurrency utilities
- Error handling infrastructure

**Key considerations (from Design Doc 0020):**

- Immutable data in Go requires careful design
- Performance through structural sharing
- Interface design for extensibility
- Interop with Go's native types

**Generated code example:**

```go
import "github.com/zylisp/runtime/collections"

// Generated from Zylisp code
func myFunction() collections.List {
    return collections.NewList(1, 2, 3).Cons(0)
}
```

**Why it matters:** Every compiled Zylisp program imports this. The runtime's performance, correctness, and API design directly impact all Zylisp code.

---

### **zylisp/rely**

*Supervision trees for process management*

**Purpose:** Erlang-inspired fault tolerance for Go/Zylisp systems.

- Supervision tree implementation (Design Doc 0030)
- Management of both OS processes and goroutines
- Built on `suture` library with custom extensions
- Restart strategies and policies
- Health checking and monitoring
- Graceful shutdown handling

**Supervision strategies:**

- One-for-one: restart only failed child
- One-for-all: restart all children if one fails
- Rest-for-one: restart failed child and those started after it

**Use cases:**

- Long-running services with multiple components
- Fault-tolerant distributed systems
- Process pools and worker management
- Resource cleanup and lifecycle management

**Why it matters:** Drawing from Erlang/OTP's proven model, `rely` enables building robust systems where failures are expected and handled gracefully. This is crucial for production systems.

---

### **zylisp/core**

*Shared foundational code across repositories*

**Purpose:** Common utilities and infrastructure used project-wide.

- Source map implementation (Design Doc 0022)
- Code position tracking for debugging
- Error reporting with accurate source locations
- Debug information structures
- Shared interfaces and data structures
- Common utilities

**Key feature:** Source maps enable excellent error messages:

```
Error in myfile.zy:42:17
  | (defn factorial [n]
  |                 ^ Type mismatch: expected int, got string
```

**Relationship to other repos:**

- Used by `lang` for macro expansion error reporting
- Used by `zast` for tracking transformations
- Used by `repl` for interactive error display
- Used by compiler for final error messages

**Why it matters:** Good error messages make the difference between a frustrating and pleasant development experience. `core` ensures consistency across the entire toolchain.

---

## Quality Assurance

### **zylisp/go-ast-coverage**

*Completeness verification for Go AST support*

**Purpose:** Systematic validation that ZAST can represent all Go constructs.

- Test files covering every Go AST node type
- Automated coverage reports
- Gap analysis for unsupported features
- Edge case test suite
- Regression tests for AST translation

**Testing approach (from Design Doc 0012):**

- Generate Go code using every AST construct
- Convert to ZAST
- Verify round-trip conversion
- Check that generated code compiles
- Document any limitations

**Current coverage targets:**

- ✓ Basic declarations (Phase 2)
- ✓ Control flow (Phase 3)
- ✓ Complex types (Phase 4)
- ✓ Advanced features (Phase 5)
- ⧗ Final polish (Phase 6)

**Why it matters:** Since Zylisp aims to provide full access to Go's capabilities, this repo ensures nothing is missed. It's quality assurance for the core compilation pipeline.
