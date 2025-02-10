This repository demonstrates a subtle bug in Lua related to the `pairs` iterator.  When iterating over a table and modifying that table during iteration (e.g., adding or removing entries), the `pairs` iterator can skip entries. This unexpected behavior can lead to hard-to-debug issues in applications.

The `bug.lua` file contains the code that exhibits this problem.  The `bugSolution.lua` file offers a solution using a copy of the table to avoid in-place modification during iteration.

This example is important for highlighting the importance of understanding how Lua iterators behave under concurrent modification.