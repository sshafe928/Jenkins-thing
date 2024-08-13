Step 1: Finding the Range of Digging
To determine the lowest and highest squares that your uncle reached, you'll need to convert the encoded digging logs into square numbers using the same method as the example. Here's how you could approach it:

Convert Each Code to a Square Number:

First, split the code into the row (FBFBBFF) and column (RLR) sections.
Follow the steps described in the example to calculate the row and column.
Convert these into a square number using the formula:
Square Number
=
(
Row
×
8
)
+
Column
Square Number=(Row×8)+Column
Find the Minimum and Maximum Squares:

Use the forEach() method to iterate through each square number and determine the lowest (minimum) and highest (maximum) values.
Step 2: Identifying Missing Squares
To identify any missing squares between the lowest and highest:

Generate a Range:

Create an array that represents all possible square numbers between the minimum and maximum.
Check for Missing Squares:

Use every(), filter(), or some() to compare your list of dug squares against this range to find any gaps (i.e., missing squares).
Step 3: Backtracking to Find Coordinates
Once you've identified the missing square, reverse the process to find the coordinates:

Reverse Calculation:

Given the missing square number, calculate the row and column:
Row
=
Square Number
÷
8
Row=Square Number÷8

Column
=
Square Number
m
o
d
 
 
8
Column=Square Numbermod8
Convert to Code:

Backtrack the process to convert the row and column back into the encoded format (like FBFBBFFRLR).
Step 4: Unlocking the Safe
To generate the 6-digit code:

Sum Rows and Columns:
Store the rows and columns from all dug squares into separate arrays.
Use reduce() to sum the total rows and columns.
Multiply and Format the Code:
Multiply these sums together.
Remove any zeros from the result to form your 6-digit code.
Step 5: Visual Representation
Finally, visualize the yard:

Map Dug Squares:
Use map() to create a grid representation.
Replace dug squares with # and undug squares with ..
Print out the grid to see the pattern of where digging occurred.