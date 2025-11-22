# Number Theory Foundations

## Theorem 1: Prime Checking up to √n

**Statement**: If a number `n > 1` is composite, then it has a prime divisor `p ≤ √n`.

**Proof**:
Let `n` be composite. Then `n = a × b` where `1 < a ≤ b < n`.

Assume for contradiction that both `a > √n` and `b > √n`. Then:
a × b > √n × √n = n
But `a × b = n`, which is a contradiction. Therefore, `a ≤ √n`.

**Conclusion**: We only need to check divisors up to `√n`.

---

## Theorem 2: Even Numbers Greater Than 2 Cannot Be Prime

**Statement**: If `n > 2` and `n` is even, then `n` is composite.

**Proof**:
Any even number `n > 2` can be written as `n = 2 × k` where `k > 1`.
Since `n` has divisors `1, 2, k, n` and `2 ≠ 1` and `2 ≠ n`, `n` is composite.

**Application**: After checking `n = 2`, we skip all even numbers.

---

## Theorem 3: Goldbach Search Space Reduction

**Statement**: For finding prime pairs `(p, q)` where `p + q = n` and `p ≤ q`, we only need to check `p` from `2` to `n/2`.
p ≤ q
p ≤ n - p
2p ≤ n
p ≤ n/2

**Application**: Loop from `2` to `n/2` inclusive.

---

## Theorem 4: Odd Number Property

**Statement**: An odd number can only have odd divisors (except 1).

**Proof**:
Let `n` be odd. If `n` had an even divisor `d`, then `n = d × k`.
Since `d` is even, `d × k` would be even, contradicting that `n` is odd.

**Application**: After checking divisibility by 2, we only check odd divisors.

---

## Corollary: Step Size Optimization

Since we:
1. Handle `n = 2` separately
2. Reject even `n > 2`
3. Only check odd divisors for odd `n`

We can iterate with `step = 2` in our prime checking loop.

---

## Mathematical Summary

Our algorithm leverages these number theory principles:
- **Divisor bound**: Check only up to √n
- **Parity**: Skip even numbers after 2  
- **Search space**: Only check p ≤ n/2 for Goldbach pairs
- **Step optimization**: Check only odd potential divisors

These optimizations reduce time complexity from O(n²) to O(n√n).

**Proof**:
We require `p ≤ q` and `p + q = n`. Therefore:
