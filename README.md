Adder Compiler

This project implements a compiler for the Adder language.

The compiler reads a .snek file containing an expression and generates x86-64 assembly code. The result of the expression is stored in the rax register and printed by the runtime.

**Supported Language Features**
- 32-bit signed integers
- (add1 e)
- (sub1 e)
- (negate e)
- Nested expressions

**How to Build and Run**
From the project root directory:
make test/test_name.run
./test/test_name.run


**Example:**
make test/test_add1_basic.run
./test/test_add1_basic.run

**Compilation Pipeline** 
The compiler works as follows:
- Parse .snek source into an AST.
- Generate x86-64 assembly.
- Assemble using NASM.
- Link with the runtime.
- Execute the final program.
