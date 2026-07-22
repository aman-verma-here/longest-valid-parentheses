# Longest Valid Parentheses

## Problem Statement

Given a string containing only the characters '(' and ')', return the length of the longest valid (well-formed) parentheses substring.

### Example 1
Input:
```
s = "(()"
```

Output:
```
2
```

### Example 2
Input:
```
s = ")()())"
```

Output:
```
4
```

### Example 3
Input:
```
s = ""
```

Output:
```
0
```

---

## Approach

This solution uses a **Stack** to store indices of parentheses.

- Push `-1` initially as the base index.
- Push the index of every `'('`.
- For every `')'`, pop one index.
- If the stack becomes empty, push the current index.
- Otherwise, calculate the current valid substring length using:
```
currentLength = currentIndex - stack.peek()
```
- Keep updating the maximum length.

---

## Time Complexity

**O(n)**

## Space Complexity

**O(n)**

---

## Language

Java
