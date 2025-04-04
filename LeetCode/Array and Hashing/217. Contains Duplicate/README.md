# 217. Contains Duplicate
Link: [Contains Duplicate](https://leetcode.com/problems/contains-duplicate/description/)\
Difficulty: Easy\
Topics: Array, Hash

=======================================================================================

## Clarify
1. Can the input array be empty?
2. Any requirement on time/space complexity?
   - Time Complexity: O(N)
   - Space Complexity: O(N)
3. Is the array sorted?
## Match
1. Hash Set\
   As we iterate through the array, we can storeeach number in a Set. If the number is already in the set, then we can return true. If the number has not been seen, we can store it in the Set. If we reach the end of the array, then return false.
2. Hash Set Length\
   Compare the length of the set with the length of the array. If the length of the set is smaller, it means there are repeated numbers in the array.
## Plan
General Idea 1: Create a set to store the numbers in the array. If the number hasn't been seen, store it in the set. If the current number has been seen, return true.
1. Create a set.
2. For each number in the array, check if the current number is already in the set. If yes, return true.
3. If no, store the current number in the set.
4. Return false if we reach the end of the array.

General Idea 2: Compare the length of the set and the array.
1. Use len() and set() to get the length of the set.
2. Return the comparing result. If the length of the set is smaller, return true. Otherwise, return false.
## Evaluate
- Time Complexity: O(N)
- Space Complexity: O(N)

