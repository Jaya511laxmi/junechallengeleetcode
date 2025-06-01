### 📅 Day 01 – Distribute Candies Among Children II

- 🔗 **LeetCode Problem**: [2929. Distribute Candies Among Children II](https://leetcode.com/problems/distribute-candies-among-children-ii/)
- 💡 **Difficulty**: Medium  
- 🧠 **Topic Tags**: Math, Combinatorics, Brute Force  

---

### ✍️ Problem Summary

You are given two integers: `n` (the number of candies) and `limit` (maximum candies a child can receive). Distribute candies among **3 children** such that:
- Each child gets between 0 and `limit` candies (inclusive),
- Total candies distributed is exactly `n`.

You need to return the **total number of valid distributions**.

---

### 🚧 My Approach

- Let’s fix the candies for **Child 1** in the range `[max(0, n - 2 * limit), min(n, limit)]`.
- For each valid value of `Child 1`, compute how many valid values are possible for **Child 2** such that:
  - `Child 2` lies in `[max(0, remaining - limit), min(remaining, limit)]`, where `remaining = n - candies_child1`.
- The value of **Child 3** gets automatically fixed as `n - (Child 1 + Child 2)`.
- We count the number of valid combinations using a loop over possible values of Child 1 and a mathematical range count for Child 2.

---

### 😖 Struggles

- Initially tried brute-force, but it failed due to time constraints.
- Had to mathematically limit the loop ranges to avoid TLE.
- Needed to be careful with edge cases like when `n < 3` or `limit` is too small.

---

### ✅ What I Learned

- Efficient counting using **range limits** instead of nested loops.
- Importance of **combinatorics** and **mathematical observations** in coding problems.
- Sometimes, fixing one variable and deriving others from constraints helps prune the search space drastically.
