# 3. Longest Substring Without Repeating Characters
Link: [Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/description/)\
Difficulty: Medium\
Topics: String, Sliding Window

=======================================================================================\

## Clarify
1. Can the input be empty?
   - No.
2. Any requirement on time/space complexity?
3. Are the characters case-sensitive? For example, is 'a' different from 'A'??
   - Yes.
## Match
1. Sliding Window\
   Use the sliding window by setting the left and right boundaries. Iterate through the given string to find the largest window.
## Plan
General Idea: Set index `left` and `right` to generate a sliding window. If a dulpicate is found, move the sliding window.
1. Initialize the left boundary `left` and `result`.
2. Iterate through the given string. If a duplicate is found, move `left` to remove the first found character to remove the duplicate.
3. Get the result by calculating the length of the sliding window.
## Review
I didn't realize that I should slide the window to remove the first found duplicating character, not skipping the second found character.
## Evaluate
- Time Complexity: O(N)
- Space Complexity: O(M)
