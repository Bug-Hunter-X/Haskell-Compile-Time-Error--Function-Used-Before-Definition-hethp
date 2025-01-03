# Haskell Compile-Time Error: Function Used Before Definition

This repository demonstrates a common compile-time error in Haskell where a function is used before it is defined.  The error arises because Haskell evaluates code sequentially and functions must be defined before they are called.

## Bug

The `bug.hs` file contains the erroneous code. The `mysteryFunction` is used in `main` before its definition, which results in a compiler error.

## Solution

The `bugSolution.hs` file shows the corrected code. The function definition is placed *before* its usage. This allows the compiler to find the definition when `main` calls `mysteryFunction`.

## How to reproduce

1. Clone the repository.
2. Navigate to the repository directory in your terminal.
3. Load the `bug.hs` file into a Haskell compiler (such as GHC). You should observe a compile-time error.
4. Load the `bugSolution.hs` file. This will compile successfully.