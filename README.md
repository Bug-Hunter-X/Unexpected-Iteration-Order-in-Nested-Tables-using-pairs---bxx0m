# Lua Nested Table Iteration Issue

This repository demonstrates a potential issue with Lua's `pairs` iterator when dealing with nested tables.  The `pairs` function does not guarantee a specific iteration order, which can lead to unexpected behavior if your code relies on a particular order.

The `bug.lua` file contains code that iterates through a nested table.  The `bugSolution.lua` file offers a potential solution using a different approach.

## Problem

The `bug.lua` example shows how relying on the order of `pairs` can lead to unexpected results when processing nested tables.  The order of iteration is not defined and may vary between Lua versions or implementations.

## Solution

The `bugSolution.lua` example demonstrates a way to achieve a consistent iteration order. The solution involves sorting the keys before iterating to achieve deterministic behavior.