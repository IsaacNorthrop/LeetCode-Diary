# LeetCode-Diary
Isaac Northrop's journey through LeetCode.
## Entries

	88. Merge Sorted Array

Use two pointer approach. Initialize pointers to the end of the numbers in the first array (before zeros), the end of the second array, and the very end of the first array, called the input position. Until you reach the beginning of one of the arrays, compare each entry in each array, and put the larger one in the current input position, then decrement the input position. If you reach the end of the first array first, put the rest of the numbers from the second array in the first.

Eg.
![image](https://github.com/user-attachments/assets/f284da96-bd86-4e5a-931b-3dc56360a0c9)
![image](https://github.com/user-attachments/assets/8e695d36-883e-4185-a6f0-f2c00db6be18)
![image](https://github.com/user-attachments/assets/57220344-737a-457b-b618-ff8f7ba9ebf2)






