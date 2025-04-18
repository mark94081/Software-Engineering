# 11. Container With Most Water
Link: [Container With Most Water](https://leetcode.com/problems/container-with-most-water/description/)\
Difficulty: Medium\
Topics: Array, Two Pointers

=======================================================================================\

## Clarify
1. Can the input be empty?
   - No, there is exactly one solution.
2. Any requirement on time/space complexity?
3. Is the input list sorted?
   - No.
## Match
1. Two Pointers\
   Use two pointers, one from the start and the other from the end of the list. 
## Plan
General Idea: Use two pointers to keep finding the maximum. Move the pointer that points to a smaller height value.
1. Initialize two pointer `left` and `right`, one from the start and the other from the end of the list. Set the maximum to 0.
2. If the current area is larger than the local maximum, update the local maximum.
3. If the height pointed by `left` is smaller than that pointed by `right`, `left += 1`.
4. Otherwise, `right -= 1`.
## Review
In the beginning, I thought I should move the pointer by checking if the next height value makes a larger area. But I should only move the pointer by checking which height value pointed by two pointers is smaller.
## Evaluate
- Time Complexity: O(N)
- Space Complexity: O(1)
