---
layout: post
title:  "Number Representation"
categories: notes
tag: notes
---

Here are some notes on the representation of numbers by computer systems. Three main representations will be included here: 1) *unsigned*, 2) *two's complement*, and 3) *floating point*.

## Representing Integers

There are two ways of representing integers, depending on whether we want the numbers to be signed or unsigned.

### Unsigned

- The unsigned representation encodes integers based on traditional binary notation.
  - E.g. $1010_2 = 2^3 + 2^1 = 8$.
- **Minimum**: For a word size of $w$, the minimum is $00...000$, with $w$ 0's. The minimum is thus: $$UMin = 0$$
- **Maximum**: For a word size of $w$, the minimum is $11...111$, with $w$ 1's. The maximum is thus: $$UMax = 2^w - 1$$

### Two's Complement

- Two's complement is the most common computer representation of signed numbers.
- The most significant bit of the word is the **sign bit** and is defined to have a negative weight.
  - E.g. $1010_2 = -2^3 + 2^1 = -7$.
- **Minimum**: For a word size of $w$, the minimum is $100...00$, with a leading $1$ followed by a trail of $0$'s. The minimum is thus: $$TMin = -2^{w-1}$$
- **Maximum**: For a word size of $w$, the maximum is $011...11$, with a leading $0$ followed by a trail of $1$'s. The maximum is thus: $$TMax = 2^{w-1} - 1$$

### Converting between Signed and Unsigned

In C, we can cast between signed and unsigned numbers: for example, the expression `(unsigned) x` converts `x` to an unsigned value, while `(int) x` converts it to a signed integer.

When we convert between signed and unsigned values, the binary representation does not change. In other words, the bit values themselves do not change, but rather, we only change the interpretation of these bits. For example, -13 as a signed number becomes 19, for both are represented by the bits 10011.

## Floating Point

- Overflow will yield the special value of [positive infinity].