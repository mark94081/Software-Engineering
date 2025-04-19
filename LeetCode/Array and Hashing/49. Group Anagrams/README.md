# 15. 3Sum
Link: [3Sum](https://leetcode.com/problems/3sum/description/)\
Difficulty: Medium\
Topics: Array, Hash Table

=======================================================================================\

## Clarify
1. Can the input be empty?
   - Yes. The return ans will be `[[""]]` in this case.
2. Any requirement on time/space complexity?
   - It should be better than O(NM*logM).
3. Only ascii characters?
   - The string only contains lowercase letters.
## Match
1. Hash Table\
   Create a hash table, the keys are the frequency lists and the values are the groups of the strings.
## Plan
General Idea: Use the hash table, and the key is the frequency list and the value is the group of strings.
1. Initialize a hash table.
2. Iterate through the list of strings:
   - Use a list to record the frequency of the string.
   - Add the string into the hash table based on its frequency list.
3. Convert the values of the hash table to the list and return it.
## Review
I didn't know the key of hash table can be a list.
## Evaluate
- Time Complexity: O(M*N)
- Space Complexity:
  - O(M) extra space.
  - O(M*N) space for the output list.
