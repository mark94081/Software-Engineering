# 53. Maximum Subarray
Link: [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/description/)\
Difficulty: Medium\
Topics: Kadane's Algorithm

=======================================================================================\

## Clarify
1. Can the input be empty?
2. Any requirement on time/space complexity?
3. Is the array sorted?
## Match
1. Kadane's Algorithm\
   Determine either add the current elements to the current sum or start a new subarray by resetting the current sum. Record the global maximum.
## Plan
General Idea: Use a variable `curSum` to track the sum of the elements. At each index, we have two choices: either add the current element to `curSum` or start a new subarray by resetting `curSum` to the current element. Track the maximum sum at each step and update the global maximum accordingly.
1. Create two variables to record the current sum and global maximum.
2. Iterate  `nums` list. If `curSum`  is negative, resetting it. Else, add the current element to `curSum`. 
3. Compare the current sum with the global maximum.
## Evaluate
- Time Complexity: O(N)
- Space Complexity: O(1)


