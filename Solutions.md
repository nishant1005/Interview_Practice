# Interview_Practice
Udacity/Leet Code Questions

# Q1 Given two strings s and t, determine whether some anagram of t is a substring of s. For example: 
if s = "udacity" and t = "ad", then the function returns True.
Your function definition should look like: question1(s, t) and return a boolean True or False.

Solution 1)Here we first check the validitiy of the test by comparing size of string T to S,and if T is bigger, the input is deemed invalid.
Now in order to check for anagram,i have runned thorugh every character in string s one by one and checkeed whether any character is present in string t.If it is present,then i have removed this character iteratively.Now,if string t's characters(2 characters) are matched and removed=,length of this string will be zero,hence we have an anagram.
