# Variables and Mutability
[Back to index](../index.md)

---

## Variables
- Variables are defined with the keyword `let`.
- By default they are inmmutable.
- They are made mutable with the keyword `mut`.
- By convention they are writen in lower case but the first letter of each word (instead the first).

```Rust
let myVariable = 5;    // It should be let mut myVariable = 5
    myVariable = 6;    // Error, immutable variable.
```

## Constants
- Constants are defined with the keyword `const`.
- By convention they are writen in capital letters separed by underscores.
```Rust
const MY_CONSTANT = 7;
```

## Shadowing
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