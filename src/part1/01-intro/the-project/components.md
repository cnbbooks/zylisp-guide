# How It All Fits Together

**The compilation pipeline:**

1. **Developer writes** Zylisp code in `.zy` files
2. **REPL** (from `repl`) provides interactive development and testing
3. **Parser** reads s-expressions and builds initial AST
4. **Macro expander** (in `lang`) processes macros and special forms
5. **Forms pipeline** (in `lang`) transforms Zylisp-specific constructs
6. **ZAST generator** converts expanded code to Go AST s-expressions
7. **Code generator** produces readable Go source files
8. **Generated code** imports `runtime` for data structures and support
9. **Error messages** use source maps from `core` for accurate reporting
10. **Production systems** use `rely` for supervision and fault tolerance
11. **Coverage tests** (in `go-ast-coverage`) verify completeness

**Design feedback loop:**

1. Feature idea or problem identified
2. Design document created in `design` repo
3. Discussion and iteration (Draft → Under Review → Final)
4. Implementation planned with phase assignments
5. Code written in appropriate repo (`lang`, `zast`, `runtime`, etc.)
6. Tests added to verify correctness
7. Documentation updated
8. Experience feeds back into design process
