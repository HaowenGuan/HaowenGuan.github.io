# Python Note

## Bit Manipulation
1. `^`: Bitwise XOR. (logically same as `!=`)
   1. `0 ^ 0 = 0`, `1 ^ 0 = 1`, `0 ^ 1 = 1`, and `1 ^ 1 = 0`.
   2. `1 ^ 2 = 3 `, since `(01) ^ (10) = (11)`.
   3. `x ^ 0 = x`, `x ^ x = 0`, thus `x ^ y ^ x = (x ^ x) ^ y = 0 ^ y = y.`
2. `&`: Bitwise AND.
   1. `0 & 0 = 0`, `1 & 0 = 0`, `0 & 1 = 0`, and `1 & 1 = 2`.
   2. `2 & 3 = 1`, since `(10) & (11) = (01)`.
   3. `5 & 1 = 1`, since `(101) & (001) = (001)`
3. `<<` or `>>`: Bitwise Shift Operators.
   1. `1 << 2 = 4 `, since `(001) << 2 = (100)`