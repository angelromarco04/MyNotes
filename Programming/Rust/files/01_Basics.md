# Basics
[Back to index](../index.md)

---
## Introduction to Rust
### Compiler
A rust file (`.rs`) can be compiled with the command `rustc my_program.rs` 
Then a binarie `my_program.exe`in windows or `my_program` in linux will be created.
It can be executed with `.\my_program.exe` in windows or `./my_program` in linux.

### Cargo
Cargo is Rust’s build system and package manager.
- The version installed can be checked: `cargo --version`
- To create a new project: `cargo new my_project`
- To build the project: `cargo build`
- To run the project (will also buid if needed): `cargo run`
- To check if the program compiles without actually doing it: `cargo check`

## Variables and Mutability

### Variables
- Variables are defined with the keyword `let`.
- By default they are inmmutable.
- They are made mutable with the keyword `mut`.
- By convention they are writen in lower case but the first letter of each word (instead the first).

```Rust
let myVariable = 5;    // It should be let mut myVariable = 5
    myVariable = 6;    // Error, immutable variable.
```

### Constants
- Constants are defined with the keyword `const`.
- By convention they are writen in capital letters separed by underscores.
```Rust
const MY_CONSTANT = 7;
```

### Shadowing
- This allows to redefine a variable with the same name and a another value.
- This value will only be used in the scope it was redefined in.
  
```Rust
let x = 5;
    {
        let x = x * 2;
        // x inside the brackets will be 10
    }
// Here x will be 5 again
```

## Data types
- Rust must know the types of all variables at compile time.
- The compiler can usually infer the type.
- In cases when many types are possible, it must be specified.
    ```Rust
    let var: datatype;
    ```
- There are two main types: scalar and compound.

### Scalar
- Are tipes that represent a single value

#### Integer
|Length   | Signed | Unsigned |
|---------|--------|----------|
| 8-bit   | i8     | u8       |
| 16-bit  | i16    | u16      |
| 32-bit  | i32    | u32      |
| 64-bit  | i64    | u64      |
| 128-bit | i128   | u128     |
| arch    | isize  | usize    |

- `arch` depends on the architecture (64-bit or 32-bit)
- Signed integers are stored using two's complement.
- By default: `i32`.
- Can be specified in Dec (`14`), Hex (`0x e`), Octal (`0o 16`) or Bin (`0b 1110`).
- If `u8`, also expressed as Byte (`b'E'`)

#### Floating point
- As the integers there exist from `f8` to `f128` (varying the size).
- All floating point values are signed.
- By default: `f64`

#### Boolean
- Can be `true` or `false`.
- Explicitely defined with `bool`.

#### Character
- Explicitely defined with `char`.
- Characters use simple quotes (`'A'`).
- It is 4-byte wide represented in Unicode Scalar Value

### Compound
TODO
