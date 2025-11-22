# Goldbach Conjecture

## Introduction
The Goldbach Conjecture is a famous unsolved problem in mathematics proposed by Christian Goldbach in 1742. It states that:

> **Every even integer greater than 2 can be expressed as the sum of two prime numbers.**

For example:
- 4 = 2 + 2
- 6 = 3 + 3  
- 8 = 3 + 5
- 10 = 3 + 7 or 5 + 5

## Your Task
Write a Python function that finds **all possible pairs of prime numbers** that add up to a given number.

## What We Want in Python

```python
def goldbach_partitions(n):
    """
    Find all prime pairs that sum to n.
    
    Args:
        n: integer to check (3 ≤ n ≤ 3000)
    
    Returns:
        List of strings in format "p+q" where:
        - p and q are prime numbers
        - p + q = n
        - p <= q (to avoid duplicates)
        - Sorted by increasing p value
    goldbach_partitions(10)   # → ["3+7", "5+5"]
    goldbach_partitions(26)   # → ["3+23", "7+19", "13+13"]
    goldbach_partitions(100)  # → ["3+97", "11+89", "17+83", "29+71", "41+59", "47+53"]
    goldbach_partitions(7)    # → []  (odd number)
    
    Returns empty list if n is odd.
    """
