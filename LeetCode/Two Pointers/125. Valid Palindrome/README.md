# 125. Valid Palindrome
Link: [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/description/)\
Difficulty: Easy\
Topics: String, Two Pointers

=======================================================================================\

## Clarify
1. Are there any specific edge cases you'd like the solution to handle? For example, empty strings, strings with only one character, or strings with only non-alphanumeric characters?
   - You should handle all of them.
2. Any requirement on time/space complexity?
## Match
1. Two Pointers\
   Use two pointers, one from the start and the other form the end.
## Plan
General Idea: Use two pointers check if the characters pointed by two pointers are the same.
1. Initialize two pointers `left` and `right`.
2. Check if the character is alphanumeric. If not, skip it and move the pointer to the next one.
3. Check if the characters pointed by two pointers are the same. If not, return False.
4. Move two pointers to point to the next one until `left` >= `right`.
5. If each step of checking is good, return True.
## Review
I didn't know I can use `s[left].isalnum()` to check if a character is alphanumeric.
## Evaluate
- Time Complexity: O(N)
- Space Complexity: O(1)
