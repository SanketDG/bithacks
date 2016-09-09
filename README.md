# Bit Hacks

A collection of bit manipulation techniques.

## Multiply a number by 2

```
n << 1
```

## Divide a number by 2

```
n >> 1
```

## Check if a number is a power of two

```
n & (n-1) == 0
```

## Minimum and Maximum of two numbers

```
r = y ^ ((x ^ y) & -(x < y))
```

Note that 0 is incorrectly considered a power of 2 here. To remedy this, use:

```
f = v && !(v & (v - 1));
```
