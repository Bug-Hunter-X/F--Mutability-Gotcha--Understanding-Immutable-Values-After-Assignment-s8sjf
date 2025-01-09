# F# Mutability Gotcha: Understanding Immutable Values After Assignment

This repository demonstrates a subtle but common issue in F# related to mutability and the behavior of values after assignment. The example highlights how a variable calculated from mutable values remains fixed if not reassigned even if the source values change.

## The Bug

The `bug.fs` file contains code that initializes mutable variables `x` and `y`. A variable `z` is calculated as their sum. Despite subsequent modifications to `x` and `y`, `z` retains its initial value. This behavior might be unexpected for programmers unfamiliar with F#'s immutability model. 

## The Solution

The `bugSolution.fs` file offers a corrected version. To ensure `z` reflects changes in `x` and `y`, it's recalculated after modifications or a function is used to make `z` dependent on the mutable values.