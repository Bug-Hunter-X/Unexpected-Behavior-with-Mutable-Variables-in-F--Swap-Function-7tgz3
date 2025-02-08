# F# Mutable Variable Swap Bug

This repository demonstrates a common bug in F# related to the use of mutable variables and pass-by-reference semantics.  The `swap` function intends to exchange the values of two variables, but due to the nature of mutable variables in F#, the original variables are directly modified.  The solution showcases a correct approach using tuples to avoid unexpected side effects.

## Bug Description

The `bug.fs` file contains code that attempts to swap two mutable variables. However, because F# passes mutable variables by reference, the swap function modifies the original variables, resulting in an incorrect outcome. 

## Solution

The `bugSolution.fs` file provides a corrected implementation using tuples.  Tuples are immutable, preventing unintended modifications to the original variables. This approach ensures that the swap operation doesn't affect variables outside of the function's scope.
