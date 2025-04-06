# 238. Product of Array Except Self
Link: [Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/description/)\
Difficulty: Medium\
Topics: Array, Presum (Prefix, Suffix)

=======================================================================================

## Clarify
1. Can the nums array be empty?
   - There are the minimum input of two numbers.
2. Any requirement on time/space complexity?
   - Solve in O(1) extra space complexity.
## Match
1. Presum\
   Create a list to store the products. First, store the product of all numbers to the left of each element. Then, Multiply the product of all numbers to the right of each element in the array by the corresponding element in the list.
## Plan
General Idea: For each element in the array, multiply the product of all numbers to the left of it first and store it in the list. Then, multiply the product of all numbers to the right of each element in the array by the corresponding element in the list.
1. Create a list to store the products.
2. For each element in the array, store the product of all numbers to the left in the list. Calculate the the product of all numbers to the left of next element.
3. For each element in the list, multiply it by the product of all numbers to the right of the corresponding element in the array.
## Evaluate
- Time Complexity: O(N)
- Space Complexity: 
  - O(n) space for the output array.
  - O(1) extra space.
