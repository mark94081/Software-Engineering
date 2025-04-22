# 5. Longest Palindromic Substring
Link: [Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/description/)\
Difficulty: Medium\
Topics: String, Two Pointers

=======================================================================================\

## Clarify
1. Can the input be empty?
   - No.
2. Any requirement on time/space complexity?
3. Does the string only contain digits and English letters?
   - Yes.
## Match
1. Two Pointers\
   Use two pointers to find if the left side and the right side of each center are the same.
## Plan
General Idea: Use two pointers to check if the left side and right side of each element are the same and record the string and its length.
1. Initialize the result list and the length of the result list.
2. Find the palindrome with the odd length and even length separately:
   - For the odd length, set both `left` and `right` to `i` and iterate both sides of each element to check if the elements pointed by the left pointer and the right pointer are the same. If they are the same, check if the length of the substring is bigger than the local maximum. If yes, record the substring and its length, and move `left` to `left - 1` and `right` to `right + 1`.
   - For the even length, set `left` to `i` and `right` to `i + 1` and iterate both sides of each element to check if the elements pointed by the left pointer and the right pointer are the same. If they are the same, check if the length of the substring is bigger than the local maximum. If yes, record the substring and its length, and move `left` to `left - 1` and `right` to `right + 1`.
3. Return the substring that has the largest length.
## Review
I didn't realize that I should notice two possibilities of the odd and even length.
## Evaluate
- Time Complexity: O(N^2)
- Space Complexity:
  - O(1) extra space.
  - O(N) space for the output string.
