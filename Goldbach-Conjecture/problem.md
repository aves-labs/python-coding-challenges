# Goldbach Conjecture Problem

## The Problem
Write a function that finds all possible ways to represent an even number as the sum of two prime numbers.

```python
def goldbach_partitions(n):
    """
    For even n >= 4, find all pairs of prime numbers (p, q) where:
    - p + q = n
    - p <= q (to avoid duplicates like 3+5 and 5+3)
    - Return as list of strings: ["p+q", "p+q", ...]
    
    For odd n or n < 4, return empty list.
    
    Examples:
    goldbach_partitions(10) → ["3+7", "5+5"]
    goldbach_partitions(26) → ["3+23", "7+19", "13+13"] 
    goldbach_partitions(7) → []
    """
    # Your code here
