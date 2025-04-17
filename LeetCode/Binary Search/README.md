# 33. Search in Rotated Sorted Array
Link: [Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/description/)\
Difficulty: Medium\
Topics: Array, Two Pointers, Binary Search

=======================================================================================\

## Clarify
1. Can the input be empty?
   - We don't need to consider empty inputs.
2. Any requirement on time/space complexity?
   - O(log n)
3. Will there be negative numbers?
   - Yes.
## Match
1. Two Pointers\
   Use two pointers `left` and `right` to narrow down the range.
## Plan
General Idea: Use two pointers to keep splitting the array into the sorted and unsorted subarraies. In this way, we can narrow down the range efficiently and correctly without interferenced by the pivot.
1. Initialize two pointers. Set `left` and `right` pointers to the start and end of the array separately.
2. Start binary search loop: Begin a while loop that continues as long as left is less than or equal to right.
3. Find the medium point `mid` of `left` and `right` for the binary search. If `mid` equals to the target, return it.
4. Identify sorted half:
   - If the left half of the array (from `left` to `mid`) is sorted:
     - Check if the target is within this sorted left half. If yes, adjust the `right` pointer to `mid` - 1 to focus the next search in this half.
     - Otherwise, adjust the `left` pointer to `mid` + 1 to search in the right half.
   - If the left half is not sorted, then the right half must be sorted:
     - Check if the target is within the sorted right half. If yes, adjust the `left` pointer to `mid` + 1.
     - Otherwise, adjust the right pointer to `mid` - 1 to search in the left half.
5. If the loop ends without returning, it means the target is not in the array. Return -1 in this case.
## Review
When I first thought of the question, I knew I should use the binary search, but I didn't know how to implement it. I didn't have the concept of considering the position of the pivot.
## Evaluate
- Time Complexity: O(log N)
- Space Complexity: O(1)


