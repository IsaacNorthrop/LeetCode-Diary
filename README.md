# LeetCode-Diary
Isaac Northrop's journey through LeetCode.
## Entries

	88. Merge Sorted Array

Use two pointer approach. Initialize pointers to the end of the numbers in the first array (before zeros), the end of the second array, and the very end of the first array, called the input position. Until you reach the beginning of one of the arrays, compare each entry in each array, and put the larger one in the current input position, then decrement the input position. If you reach the end of the first array first, put the rest of the numbers from the second array in the first.

Eg.
![image](https://github.com/user-attachments/assets/f284da96-bd86-4e5a-931b-3dc56360a0c9)
![image](https://github.com/user-attachments/assets/8e695d36-883e-4185-a6f0-f2c00db6be18)
![image](https://github.com/user-attachments/assets/57220344-737a-457b-b618-ff8f7ba9ebf2)

	27. Remove element
Use vec.erase(location using iterator)
Make sure to decrement the vector iterator, so that you don't skip any elements.
Return size

	26. Remove Duplicates
Start at 1, first element is always unique. Compare i with i-1, if they are the same, remove i using vec.erase(), decrement i to not miss any items.
Return vector size

	169. Majority element
Initialize a current value variable, and a count variable, loop through the array
If the count is zero, there is a new majority, so set the curr to the current value in the array
If curr equals the current number, increment the count
Else decrement the count
Return curr

![image](https://github.com/user-attachments/assets/d9df1442-3765-4d77-9e85-55097174fd2b)

	121. Best time to sell stock
Start by initializing the minPrice to the first element in the array. Initialize a total profit variable at zero. Iterate from the second element. If you find a lower price, update minPrice. If you find higher local profit, update the profit. The hard part here is knowing that you have to track profits from the current lowest price, instead of finding the highest and lowest price and subtracting them to get a profit.

	58. Length of last word
Initialize a stringstream with the string in it, a vector to put the words in, and a string for the stringstream to send words into. While the stringstream can still send words, push words into the vector. Return the length of the last string in the vector.
A stringstream can write to strings, and can have strings write to it

	14. Longest common prefix
Initialize a string to the first string in the strings vector as the current prefix. Loop through the vector, for every word in the vector, loop to the length of the current prefix to minimize runtime. Loop until the letters in the current string and the current prefix don't match, then set the current prefix to the substring before the letter that doesn't match. If the length of the current prefix is 0, return "". Otherwise, finish the loop and return the current prefix.

![image](https://github.com/user-attachments/assets/ce6189b9-5259-463c-9efc-78552c9d2fdb)

	28. Find the first occurrence of a string
Check if at each letter of the haystack string, the needle exists after it. Use substr(). Check if the needle is bigger than the haystack. Loop till the length of the haystack minus length of needle.
Substr() - parameters: starting index, how long is the substr AFTER the starting index, not the total length

![image](https://github.com/user-attachments/assets/3d1346e9-0530-45a7-9d1d-d4fd9f35652e)

	125. Valid Palindrome
Go through the string and make sure all the characters in it are alphanumeric and lowercase. If the size is under 2, return true. Initialize left pointer to 0, right pointer to the size of the modified string. While left is smaller or equal to right, check if the character in the string at each pointer is equal. If not, return false. If they all are, return true.

	392. Is Subsequence
Initialize a pointer to each start of string, move subsequence index up if it matches a character in the larger string, always move up the larger index. If the index of each is the length of the string, return true

	383. Ransom note
Run through magazine and increment a hash map between the character and the number of times it appears. Run through ransom note and for every occurrence of a letter in ransom note, decrement that letter in the hash map. If any letter is greater than or equal to zero, return false.

	205. Isomorphic String
Initialize a hash map for each string, and iterate through each string. If the current character doesn't exist in the hash map, set it to the index you found that character at. If the indexes of the current characters don’t match, return false.

![image](https://github.com/user-attachments/assets/9ff8989e-bdf6-4d02-a57a-766bb8ee592e)

	209. Word Pattern
Split string with stringstream
	Issue with this is if it's only one word you have to check the length of the pattern vs the vector
Have a map from chars to words, words to chars
If the word and pattern don't have maps, map them
If either map doesn't match, return false
If everything checks out, return true

	Kadane's Algorithm
Keep track of a current maximum and the overall result. For each value in the vector, update the currentMax such that:
	Take the maximum of the current max plus the current value, and the current value. This basically makes it so that you're either extending the subarray, or you're starting a new one.
Update the result such that:
	Take the maximum of the result and the current max. This basically makes it so that you're keeping track of the current subarray, or updating to the new one.
Return result

	20. Valid Parentheses
 If the length of the string isn't even, return false;
 Initialize a stack
 for the length of the string, do the following:
	if the current value is (, [, {, push it to the stack
 	if the current value is ), ], }, and the top value of the stack is (, [, { respectively, pop
  	if not, return false
   	if the current value is ), ], } and the stack is empty, return false
If the stack is empty, return true
If it is not, return false

	242. Valid Anagram
 If the strings aren't the same length, return false
 Initialize two unordered_maps, one for each string
 iterate to the length of the strings, if a letter doesn't exists as a string, initialize a map to that key at 0
 else increment that map
 if the maps are the same, return true
 else return false

 	1957. Form Special String
if the length is less than 3, return s
Iterate through the string until 2 characters from the last one.
if the current character and the next two are the same, mark down the index of the third character, and count how many instances of the repeated character are after third one.
Use erase() to erase all those characters.
return s.
  















