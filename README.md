# Unexpected NaN with Undefined Input

This repository demonstrates a common yet subtle bug in JavaScript related to the handling of null and undefined values. The `foo` function is designed to return 0 when the input is null; however, it produces NaN when provided with undefined, due to the loose comparison (`===`).

## Bug Description

The function uses a loose comparison (`===`), causing unexpected behavior when using undefined. The strict equality (`===`) operator checks for both value and type equality.  Since `undefined` is not strictly equal to `null`, the `if` condition is skipped, and the `x + 1` operation results in `NaN` when `x` is `undefined`.