# 121. Best Time to Buy and Sell Stock
Link: [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/description/)\
Difficulty: Easy\
Topics: Array, Sliding Window

=======================================================================================

## Clarify
1. Can the nums array be empty?
2. Any requirement on time/space complexity?
   - Time Complexity: O(N)
   - Space Complexity: O(1)
3. Can prices be negative?
## Match
1. Sliding Window\
   Record the local maximum and update the max profit if the larger local maximum is found.
## Plan
General Idea: Keep updating the minimum price for calculating the local maximum profit. Return the largest local maximum profit.
1. Initialize the minimum price to the first element in the array and `max_profit` to 0.
2. For each price, check if it is smaller then the current minimum price, and update the maximim profit if `prices[i] - min > max_profit`.
3. After the iteration, we can find the largest local maximum.
## Evaluate
- Time Complexity: O(N)
- Space Complexity: O(1)
