Task 1: Case Conversion

Problem Statement:

You are provided with a string, and your task is to modify it by swapping the cases of all alphabetic characters. This means converting all lowercase letters to uppercase and all uppercase letters to lowercase.

Example:

	• Input: Campus.Credentials.com
	
	• Output: cAMPUS.cREDENTIALS.COM
		
	• Input: Pythonist 2
	
	• Output: pYTHONIST 2

Input Format

	• A single line containing a string s.

Constraints

	• The string s can contain any printable characters, including digits, symbols, and spaces.

Sample Test Case
Input:

Campus.Credentials presents "Pythonist 2".

Output:

cAMPUS.cREDENTIALS PRESENTS "pYTHONIST 2".


Solution in python:
     
		def swap_case(s):
		    return s.swapcase()
		
		
		input_string = input()
		output_string = swap_case(input_string)
		print(output_string)


![image](https://github.com/user-attachments/assets/81c507bd-74f1-4b06-9bea-bd22bda93fe2)

