# 383. Ransom Note
Link: [Ransom Note](https://leetcode.com/problems/ransom-note/description/)\
Difficulty: Easy\
Topics: Array, Hash Map

=======================================================================================\

## Clarify
1. Can the input be empty?
   - No.
2. Any requirement on time/space complexity?
3. Is the input list sorted?
   - No.
4. Does the input only contain English letters?
   - Yes. It only contains lowercase English letters.
## Match
1. Hash Map\
   Use hash maps to record the frequency of letters in two strings.
## Plan
General Idea: Use hash maps to record the frequency of letters in two strings. Compare two frequency lists. If the frequency of one of the letter in `ransomNote` is larger than that in `magazine`, return False.
1. Initialize two hash maps.
2. Use two hash maps to record the frequency of the letters in `ransomNote` and `magazine`.
3. Compare two frequency lists. If the frequency of one of the letter in `ransomNote` is larger than that in `magazine`, return False.
4. Otherwise, return True.
## Review
We can also use a dictionary to record the frequency of each letter.
## Evaluate
- Time Complexity: O(N+M)
- Space Complexity: O(1)
