# 1. Two Sum
Link: [Two Sum](https://leetcode.com/problems/two-sum/description/)\
Difficulty: Easy\
Topics: Array, Hashmap

=======================================================================================\
Given an array of integers `nums` and an integer `target`, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

Example 1:\
Input: nums = [2,7,11,15], target = 9\
Output: [0,1]\
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].

Example 2:\
Input: nums = [3,2,4], target = 6\
Output: [1,2]

Example 3:\
Input: nums = [3,3], target = 6\
Output: [0,1]

Constraints:

- 2 <= nums.length <= 10^4
- -10^9 <= nums[i] <= 10^9
- -10^9 <= target <= 10^9
- Only one valid answer exists
=======================================================================================

## Clarify
1. Can the nums array be empty?
2. Any requirement on time/space complexity?
3. Is the array sorted?
4. Will the numbers in the array duplicate?
## Match
1. Hashmap\
   Because we want to output indices, use a hashmap to store the values of the array as keys of the hashmap and store the indices of the array as values of the hashmap.
## Plan
General Idea: Create a hashmap to store indices and numbers so that we can get the index from the hashmap once we find the counterpart. (`if diff in hashmap: return hashmap[diff], i`)
1. Create a hashmap
2. `target - n` to find the counterpart
3. If we find the counterpart that is in the hashmap, return the index of the counterpart and the current index
4. Else store the current number and index in the hashmap
## Evaluate
- Time Complexity: O(N)
- Space Complexity: O(N)
