# Lua Recursive Table Traversal Bug
This repository demonstrates a potential issue with recursive table traversal in Lua using the `pairs` iterator.  The `pairs` iterator does not guarantee a specific order of iteration, which can lead to unexpected results, especially when the table structure changes during traversal.  The bug and its solution are provided in separate Lua files.

## Bug
The `bug.lua` file contains a function `foo` that recursively iterates over a table using `pairs`.  If the table's structure is modified during iteration (even indirectly), the loop might skip elements.

## Solution
The `bugSolution.lua` file presents a corrected version that utilizes a different approach, ensuring consistent traversal and preventing unexpected behavior.

## How to reproduce
1. Clone this repository.
2. Run `lua bug.lua` and observe the potential unexpected output (depending on the Lua implementation and the order `pairs` iterates).