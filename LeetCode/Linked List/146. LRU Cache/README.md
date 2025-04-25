# 146. LRU Cache
Link: [LRU Cache](https://leetcode.com/problems/lru-cache/description/)\
Difficulty: Medium\
Topics: Linked List, Hashmap

=======================================================================================\

## Clarify
1. What is an LRU?
   - A Least Recently Used (LRU) Cache organizes items in order of use, allowing you to quickly identify which item hasn't been used for the longest amount of time. An LRU cache is built by combining two data structures: a doubly linked list and a hash map.
2. Any requirement on time/space complexity?
3. Does the linked list have a cycle?
   - No.
## Match
1. Doubly Linked List\
   The doubly linked list maintains the order of elements based on their usage, allowing us to efficiently add, remove, and move elements to represent their usage.
2. Hash Map\
   The hash map provides O(1) average time complexity for lookups.
## Plan
General Idea: The hash table allows for fast access to cache items, while the doubly linked list maintains the items in order of their usage, with the most recently used items at the end. When a new item is added or an existing item is accessed, it is moved to the end of the list. If the cache exceeds its capacity, the least recently used item, found at the front of the list, is removed.
1. Get Operation:
   - Check if the key is in the hash table:
     - If it's not there, return -1.
     - If it is there, retrieve the node from the hash table.
   - Move this node to the end of the doubly linked list to mark it as recently used.
   - Return the value of the node.
2. Put Operation:
   - Check if the key is already in the cache:
     - If it is, update the value of the node and move this node to the end of the list.
     - If it's not in the cache:
       - Create a new node with the key and value.
       - Add the key and node reference to the hash table
       - Add this node to the end of the list.
       - If the cache is now over capacity:
         - Remove the node from the head of the list.
         - Remove the corresponding entry from the hash table.
3. Visualization:
   - Before Any Operation: left <-> right
   - After Some Put Operations: left <-> Node1 <-> Node2 <-> ... <-> NodeN <-> right
   - After a Get Operation on Node2: left <-> Node1 <-> ... <-> NodeN <-> Node2 <-> right
   - After Adding a New Node When at Full Capacity: left <-> Node2 <-> ... <-> NodeN <-> NewNode <-> right (Node1 is removed)
## Review
I didn't know how to build a linked list.
## Evaluate
- Time Complexity: O(1) for each `put()` and `get()` operation.
- Space Complexity: O(N)
