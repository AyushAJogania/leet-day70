# leet-day70

# Is Subsequence

## Problem Description

Given two strings `s` and `t`, return `true` if `s` is a subsequence of `t`, or `false` otherwise.

A subsequence of a string is a new string that is formed from the original string by deleting some (can be none) of the characters without disturbing the relative positions of the remaining characters. For example, "ace" is a subsequence of "abcde" while "aec" is not.

### Example 1:

**Input:** 
```
s = "abc", t = "ahbgdc"
```

**Output:** 
```
true
```

### Example 2:

**Input:** 
```
s = "axc", t = "ahbgdc"
```

**Output:** 
```
false
```

## Constraints

- 0 <= `s.length` <= 100
- 0 <= `t.length` <= 10^4
- `s` and `t` consist only of lowercase English letters.

## Solution Approach

The solution uses a two-pointer approach. It iterates through both strings, `s` and `t`, and checks if the characters in `s` appear in the same order in `t`. If so, it increments the index in `s`, and always increments the index in `t`. If `i` reaches the length of `s`, it means that all characters in `s` were found in `t` in the same order, and it returns `true`. Otherwise, it returns `false`.

The time complexity of this solution is O(n), where `n` is the length of string `t`, and the space complexity is O(1) as it uses only a constant amount of extra space.
