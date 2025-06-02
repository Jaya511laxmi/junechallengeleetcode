# 📅 Day 02 – Candy

- 🔗 **LeetCode Problem**: [135. Candy](https://leetcode.com/problems/candy/)
- 💡 **Difficulty**: Hard  
- 🧠 **Topic Tags**: Greedy, Array, Two Pointers  

---

### ✍️ Problem Summary

Given an integer array `ratings` representing the ratings of children standing in a line, distribute candies to these children following rules:
- Each child must have at least one candy.
- Children with a higher rating than their immediate neighbors must get more candies.

Return the **minimum total number of candies** needed to distribute.

---

### 🚧 My Approach

- Initialize total candies as the number of children (each gets at least one).
- Traverse the ratings to find increasing and decreasing segments:
  - For increasing sequences, increment candy counts.
  - For decreasing sequences, increment candy counts accordingly.
- Use a helper function to process segments and adjust candy counts, ensuring no double counting.
- Subtract the minimum between up and down slopes to fix overlapping peaks.
- Sum up total candies from these segments for the final answer.

---

### 😖 Struggles

- Initially tried simple left-to-right or right-to-left passes separately, which failed edge cases.
- Handling the overlap at the peak of ascending and descending sequences was tricky.
- Had to carefully implement segment processing to correctly count extra candies beyond the minimum.

---

### ✅ What I Learned

- Efficiently solving greedy problems by identifying slopes (ascending/descending).
- Importance of careful segment-based processing to avoid double counting.
- How to handle tricky edge cases involving peaks and plateaus in sequences.
