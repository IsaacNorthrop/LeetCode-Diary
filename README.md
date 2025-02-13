# LeetCode-Diary
Isaac Northrop's journey through LeetCode.
## Entries

	88. Merge Sorted Array

Use two pointer approach. Initialize pointers to the end of the numbers in the first array (before zeros), the end of the second array, and the very end of the first array, called the input position. Until you reach the beginning of one of the arrays, compare each entry in each array, and put the larger one in the current input position, then decrement the input position. If you reach the end of the first array first, put the rest of the numbers from the second array in the first.

Eg.![image](https://github.com/user-attachments/assets/39fc36dc-f5a5-40d3-b5c8-dcce8acce99a)

