StringToDoubleConversionBug
=====

Filed as [SR-2987](https://bugs.swift.org/browse/SR-2987).

This playground reproduces an issue with `Double` when multiplied by some values returns the wrong result.

Given a `Double` with a value of `4.10`.
When multiplied by `100` the result is `409.9999999999999` instead of `410`.
That can lead to all sorts of issues, for example converting to an `UInt` would return `409`.

