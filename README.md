# Unexpected Arithmetic Behavior with Boolean Values in Lua

This repository demonstrates a common pitfall in Lua programming: unexpected behavior when performing arithmetic operations on boolean values.  Lua's dynamic typing, while flexible, can lead to subtle errors if not handled carefully.

The `bug.lua` file contains code that exhibits this issue.  The `bugSolution.lua` file provides a corrected version with improved type handling.

**Issue:**

The `foo` function attempts to add 1 to a boolean value, which Lua implicitly converts to a number (true -> 1, false -> 0). This leads to unexpected results when you might expect an error or different behavior.

**Solution:**

The solution involves explicitly checking the type of the input `x` before performing arithmetic operations.  This makes the code's behavior more predictable and avoids unexpected conversions.