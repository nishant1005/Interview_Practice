# Interview_Practice
Udacity/Leet Code Questions


# Q1 Given two strings s and t, determine whether some anagram of t is a substring of s. For example: 
if s = "udacity" and t = "ad", then the function returns True.
Your function definition should look like: question1(s, t) and return a boolean True or False.


Solution 1)Here we first check the validitiy of the test by comparing size of string T to S,and if T is bigger, the input is deemed invalid.


Now in order to check for anagram,i have runned thorugh every character in string s one by one and checkeed whether any character is present in string t.If it is present,then i have removed this character iteratively.Now,if string t's characters(2 characters) are matched and removed=,length of this string will be zero,hence we have an anagram.


Time Complexity:O(n)-where n is length of string s.


Space Complexity:O(1)


**Q2)Given a string a, find the longest palindromic substring contained in a. Your function definition should look like question2(a), and return a string.


Solution2)This is a simple brute force approach for iteratively parsing thorugh each characater of a substring,and checking if its a palindrome or not.If it is a palindrome,i have stored it in an array iteratively.Then the array with largest palindromic substring is our answer.


Time Complexity-O(n2)


Space Complexity-O(1)


**Q3)Given an undirected graph G, find the minimum spanning tree within G. 
A minimum spanning tree connects all vertices in a graph with the smallest possible total weight of edges.


Solution3)Here after building the graph with unique vertices,i have sorted edges in descending order.Then we pop edges one by one until any disconnection.This will ultimately give us our MST.


Pseudo code: 1  function ReverseDelete(edges[] E)  from:https://en.wikipedia.org/wiki/Reverse-delete_algorithm
     sort E in decreasing order
    Define an index i ← 0
     while i < size(E)
       Define edge ← E[i]
          delete E[i]
          if graph is not connected
             E[i] ← edge
               i ← i + 1
    return edges[] E



Time Complexity:O(E log V (log log V)3) -E-number of edges,V-number of vertices.
Space Complexity:O(E)



**Q4)Find the least common ancestor between two nodes on a binary search tree. 


Solution4)First we find immediate parent for a node in a tree,then until the root node isn't reached i have found the oldest parent to a nodes 1 and nodes 2.Then i have checked both them share a common ancestor,and this is lest common ancestor.

Time Complexity-O(nlog(n))-n-number of nodes.
Space Complexity-O(log(n))



**Q5)Find the element in a singly linked list that's m elements from the end. For example, if a linked list has 5 elements, the 3rd element from the end is the 3rd element.


Solution5)Here i first created a linkedlist,then traversed through every node to calcluste the length.Then we find distance between total length and mth element we want to find.Now we iterative though the list again till this distance,to find the mth element.

Time Complexity:O(n)-n-number of nodes.


Space Comlexity:O(1)
