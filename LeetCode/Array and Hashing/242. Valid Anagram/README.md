# 242. Valid Anagram
Link: [Valid Anagram](https://leetcode.com/problems/valid-anagram/description/)\
Difficulty: Easy\
Topics: Hash map

=======================================================================================\

## Clarify
1. Can the input be empty?
2. Any requirement on time/space complexity?
3. Is the array sorted?
4. Will the length of two inputs be different?
## Match
1. Hashmap\
   Store alphabets of two strings in the hash map separately and record the frequency of each alphabet.
## Plan
General Idea: Create two hash maps to store alphabets and frequency of each alphabet. Compare two hash maps. If they are the same, return true. Otherwise, return false.
1. Create two hash maps.
2. Iterate two strings and store alphabets and frequency of each alphabet. Use `countS.get(s[i], 0)` to create a new index.
3. If two hash maps are the same, return true. Otherwise, return false.
## Evaluate
- Time Complexity: O(N + M)
- Space Complexity: O(1)

