# ECE 2112 Programming Assignment 2

This repository contains phyton scripts for solving various programming problems using the numerical phyton (numpy). Below are the details of each script included in this repository.

# 1) NORMALIZATION PROBLEM

Normalization is one of the most basic preprocessing techniques in
data analytics. This involves centering and scaling process. Centering means subtracting the data from the
mean and scaling means dividing with its standard deviation. Mathematically, normalization can be
expressed as:
𝑍 = (𝑋 − 𝑥̅) / 𝜎

Function : X_normalized

Description : This function will normalized random integers from a 5x5 array with their mean and standard deviation already solve and automatically input in the normalization formula.
The normalized arrays will be save and can be use for different set of codes in simple and will create shorter codes.

Example Output of normalized array : array([[-1.31176812, -0.3536442 , -0.67214301,  0.06454789,  1.27316564],
                                           [ 1.05936011, -0.29260807, -0.95544109, -0.26908915, -0.11761431],
                                           [ 1.05803706, -0.62196206,  0.80816824,  0.16209627,  0.53414269],
                                           [ 2.02835492, -2.09480763,  0.63979877, -1.65960704,  0.38624922],
                                           [-0.93258431,  0.31691698,  0.51323234, -1.05712331,  1.49432218]])


 # codes


import numpy as np  #To access numpy liblary 
# Step 1: Create a random 5x5 ndarray
X = np.random.random((5, 5))

# Step 2: Calculate the mean and standard deviation of X
mean_X = X.mean()
std_X = X.std()

# Step 3: Normalize the array
X_normalized = (X - mean_X) / std_X

# Step 4: Save the normalized array to a file
np.save('X_normalized.npy', X_normalized)





# 2) DIVISIBLE BY 3 PROBLEM

Function(s) : integers , squares , A , divisible_by_3

Description : The ''integers function'' will create an array starting from 1 to 100 or firs1 100 positive inmtegers. Using the ''squares'' function will square all positive integers. The '' A '' function will store it to reshape the array to 10x10.
Lastly , using the ''divisible_by_3'' it will find the numbers that is divisible by 3.

Output : array([  9,   36,   81,  144,  225,  324,  441,  576,  729,  900, 1089,
                 1296, 1521, 1764, 2025, 2304, 2601, 2916, 3249, 3600, 3969, 4356,
                 4761, 5184, 5625, 6084, 6561, 7056, 7569, 8100, 8649, 9216, 9801])



# codes

import numpy as np # Use to access and create numpy files

# Step 1: Create an array of the first 100 positive integers
integers = np.arange(1, 101)

# Step 2: Square each element in the array and storing in a variable
squares = integers**2

# Step 3: Reshaping the 9x9 into a 10x10 matrix and store to variable "A"
A = squares.reshape(10, 10)

# Step 4: Identify elements divisible by 3
divisible_by_3 = A[A % 3 == 0]

# Step 5: Save the result to a file
np.save('div_by_3.npy', divisible_by_3)





