# 438. Find All Anagrams in a String
Link: [Find All Anagrams in a String](https://leetcode.com/problems/find-all-anagrams-in-a-string/description/)\
Difficulty: Medium\
Topics: Sliding Window, Hash Table

=======================================================================================\

## Clarify
1. Can the input be empty?
   - No.
2. Any requirement on time/space complexity?
3. Do `s` and `p` only consisted of lowercase English letters?
   - Yes.
4. Is it possible that the length of `s` larger than that of `p`?
   - Yes.
## Match
1. Sliding Window\
   Set the left and right boundaries to form a sliding window whose length is equal to the length of the target string.
## Plan
General Idea: Create a sliding window and iterate through the string to find the substrings which are the anagram of the target string.
1. Initialize two dictionaries for recording the frequency of the letters in `s` and `p`.
2. Move the sliding window by increasing the frequency of the letter pointed by `right` and decreasing the frequency of the letter pointed by `left`.
3. If the frequency of the letter pointed by `left` is 0, pop it out.
4. If `sCount` is equal to `pCount`, add `left`to the answer list.
## Review
I didn't find that I should use hash table to record the frequency of each letter.
## Evaluate
- Time Complexity: O(N)
- Space Complexity: O(1)
