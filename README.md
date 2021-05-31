# CodeChallanges
This repository includes the python notebooks for the code challanges solved...
Each jupyter notebook includes the problem statement and code to solve the same.



### 1. Searching Challange:
Create a function to read the array of strings stored in a string array which will be a 4X4 matrix of the characters of "C","H","F" ,"O" where

"C" represents Charlie the dog
"H" reprsents its home
"F" represents dog food
"O" represents empty space in grid
GOAL

The goal is to figure out the least amount of moves required to get Charlie to grab each piece of food in the grid by moving up, down, top or left and then make it home right after.

Charlie cannot move onto the home before all pieces of food have been collected.

The grid will alwasy contain between 1 to 8 pieces of food.

Example

if strAr is ["FOOF", "OCOO", "OOOH", "FOOO"] then the least amount of steps where dog can reach each piece of food and then return hom is 11 steps.

Grid would look like

F O O F

O C O O

O O O H

F O O O

if strAr is ["FOOO", "OCOH", "OFOF", "OFOO"] then the least amount of steps where dog can reach each piece of food and then return hom is 10 steps.

Grid would look like

F O O O

O C O H

O F O F

O F O O

if strAr is ["FOOO", "OCOH", "OFOF", "OFOO"] then the least amount of steps where dog can reach each piece of food and then return hom is 10 steps.

Grid would look like

F O O O

O C O H

O F O F

O F O O

### 2. Matrix Challange:
Create a function to reas the string array parameter being passed which will make up an NXN matrix where the rows are seperated by each pair of parenthesis ( the matrix will range from 2X2 to 5X5 ).

The matrix represents connections between nodes in a graph where each node corresponds to the Nth element in the matrix (with 0 being first node).

If a connection exists from one node to another, it will be represented by a 1, if not it will be represented by 0.

e.g. If the input is a 3X3 matrix with input ["(1,1,1)","(1,0,0)","(0,1,0)"]. this means that there is a connection from node

for node 0: 0 to 0, 0 to 1 and 0 to 2
for node 1: 1 to 0
for node 2: 2 to 1.
This can be interpreted as a connection existing from node X to node Y if there is a 1 in the Xth row and Yth column.

NOTE: X to Y does not impy a connection from Y to X

GOAL

The programme should determine wheather or not the matrix, which represents connections are among the nodes, is transitive.

A "transitive relation" means that if connections "0 to 1" and "1 to 2" exists then there must exist the connection "0 to 2".

Generalized form: If there is a relatioon xRy and yRz then xRz should exists within matrix.

If matrix is completely transitive then return the string "transitive".
If it isn't, the program should return the connections needed, in the following format, in order for the matrix to be transitive: (N1,N2)-(N3,N4)-(...)
Example

You can ignore the reflexive property of nodes in answers. Return the connections needed in lexicographical order.

Input: ["(1,1,1)","(0,1,1)","(0,1,1)"]. Output: transitive
Input: ["(0,1,0,0)","(0,0,1,0)","(0,0,1,1)","(0,0,0,1)"]. Output: (0,2)-(1,3)
Input: ["(1,1,1)","(1,0,0)","(0,1,0)"]. Output: (1,2)-(2,0)
