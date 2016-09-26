# Bit Hacks

A collection of bit manipulation techniques.

*The examples are done in Python but should work with most languages
 with hardly any modification.*

## Multiply a number by 2

```python
>>> 5 << 1
10
```

## Divide a number by 2

```python
>>> 6 << 1
3
```

## Check if an integer is even or odd

```python
>>> 6 & 1 == 0
True

>>> 5 & 1 == 0
False
```

## Check if a number is a power of two

```python
>>> n = 8
>>> n & (n-1) == 0
True

>>> n = 6
>>> n & (n-1) == 0
False
```

Note that 0 is incorrectly considered a power of 2 here. To remedy this, use:

```python
>>> n = 8
>>> n and !(n & (n - 1)) == 0
True
```

## Check whether the n-th bit is set of an integer

```python
>>> n = 5
>>> n & (1 << 2) > 0 # 2nd bit is set in 101 (zero-indexed).
True

>>> n = 2
>>> n & (1 << 2) > 0 # 2nd bit is not set 010
False
```

## Minimum and Maximum of two numbers

```python
>>> x = 5
>>> y = 2
>>> y ^ ((x ^ y) & -(x < y)) # minimum
2
>>> x ^ ((x ^ y) & -(x < y)) # maximum
5
```
