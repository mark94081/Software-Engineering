# 15. 3Sum
Link: [3Sum](https://leetcode.com/problems/3sum/description/)\
Difficulty: Medium\
Topics: Array, Two Pointers

=======================================================================================\

## Clarify
1. Can the input be empty?
   - No.
2. Any requirement on time/space complexity?
3. Is the input list sorted?
   - No.
4. Can I sort the input list?
   - Yes.
## Match
1. Two Pointers\
   Use two pointers to find if there is a sum of two numbers which is equal to negative of the current number.
## Plan
General Idea: Use two pointers in the subarray behind the current number to find if there is a sum of two numbers which is equal to the current number.
1. Sort the input list.
2. Initialize two pointers `left` and `right`, where `left` starts from `i + 1` and `right` starts from the end of the list. `i` is the current index of `a`.
3. If the current number `a` is bigger than 0, stop the loop.
4. If the current number is equal to the last number, skip this run.
5. Check if the sum is equal to 0:
   - If it is too small, `left + 1`.
   - If it is too large, `right - 1`.
   - If it is equal to 0, add them to the triplets list.
     - Skip if the next `nums[left]` is equal to the previous one.
## Review
I didn't think I can use two pointers to find the sum which is equal to the negative of the current number to find the triplet sum of 0.
## Evaluate
- Time Complexity: O(N^2)
- Space Complexity:
  - O(1) or O(N) extra space depending on the sorting algorithm.
  - O(M) space for the output list.


