# Rust: Undefined Behavior with Raw Pointers and Vectors

This repository demonstrates a common error in Rust: modifying a vector through a raw pointer after borrowing it. This violates Rust's ownership rules and can lead to undefined behavior.

## The Bug

The `bug.rs` file contains code that modifies a vector using a raw pointer after borrowing the vector.  This breaks Rust's ownership system. Depending on the compiler's optimization and the system, this can cause unpredictable results. 

## The Solution

The `bugSolution.rs` file provides a correct solution.  It avoids direct pointer manipulation and uses safe Rust methods to modify the vector. 

## How to Run

1. Clone this repository.
2. Navigate to the repository directory in your terminal.
3. Run `cargo run --example bug` and `cargo run --example bugSolution` to see the results.