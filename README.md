# JavaScript Strict Equality with Null and Undefined

This repository demonstrates an uncommon error in JavaScript related to the strict equality operator (===) when comparing null and undefined values. The function `foo` unexpectedly returns 0 when the input is null and NaN when the input is undefined, showcasing a subtle difference in how JavaScript handles these two values.

## Bug Description

The provided code uses the strict equality operator (===) to check if the input `x` is null. If it is, the function returns 0. However, when the input is undefined, the expression `x + 1` results in NaN.  This behavior is not always intuitive and can be a source of unexpected errors. For instance, if a function expects a numeric value, receiving NaN can lead to further issues.

## Solution

The provided solution shows how to modify the function to handle null and undefined values more consistently and predictably.  Explicit checks for both null and undefined prevent the NaN result, making the behavior more clear and robust.