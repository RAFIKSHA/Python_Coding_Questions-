Task 2: Proper Name Capitalization

Problem Statement:
You are given a string containing words separated by spaces. Your task is to ensure that:
	• The first letter of each alphabetic word is capitalized.
	• Words that start with numbers or non-alphabetic characters should remain unchanged.
	
For example:
	• Input: "vinay raykar 12abc john doe 2abc"
	• Output: "Vinay Raykar 12abc John Doe 2abc"
	
Input:
	• A string name containing alphanumeric characters and spaces. The string will not be empty.
	
Output:
	• A string where:
		○ The first letter of each alphabetic word is capitalized.
		○ Words that begin with numbers or non-alphabetic characters are left unchanged.
		
		
Constraints:
	• The string contains alphanumeric characters and spaces only.
	• There will be no punctuation marks in the string.
	• The string length will be at most 100 characters.
	
Example 1:

Input:
	vinay raykar 12abc john doe 2abc
	
Output:
	Vinay Raykar 12abc John Doe 2abc
	
Example 2:

Input:
alison heck 1234abc Bob 987xyz
Output:

Alison Heck 1234abc Bob 987xyz
Example 3:

Input:
hello WORLD 12345
Output:

Hello World 12345
Explanation:
	• "vinay" becomes "Vinay" (alphabetic word).
	• "raykar" becomes "Raykar" (alphabetic word).
	• "12abc" remains unchanged (starts with a number).
	• "john" becomes "John" (alphabetic word).
	• "doe" becomes "Doe" (alphabetic word).
	• "2abc" remains unchanged (starts with a number)

Solution:

		def capitalize_name(name):
		    words = name.split()
		    for i in range(len(words)):
		        if words[i][0].isalpha():
		            words[i] = words[i].capitalize()
		    return " ".join(words)
		
		name = input()
    print(capitalize_name(name))
    
    
