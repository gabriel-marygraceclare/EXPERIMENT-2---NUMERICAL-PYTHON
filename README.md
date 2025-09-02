# EXPERIMENT-2---NUMERICAL-PYTHON

This reporistory contains the following assignments:
## Experiment 2: Numerical Python

Normalization Problem and Divisible By 3 Problem link:

## Normalization Problem
In this section, we are tasked to create a 5 x 5 ndarray and store it to Variable X and save the normalized array as X_Normalized.npy
1. I started by importing the NumPy library using import
```python
import numpy as np
```
2. Then I used np.random.random((5,5)) to create a 5 x 5 array with random numbers
```python
X = np.random.random((5,5))
```
3. After that, I normalized the array using the formula: Normalized = X-mean(X)/std(X)
```python
X_Normalized = (X - X.mean()) / X.std()
```
4. Then I used .save() function to save the normalized array to a .npy file
```python
np.save('X_normalized.npy', X_Normalized)
```
5. Finally, I printed the normalized array using print().
```python
print (X_Normalized)
```

## Divisible By 3 Problem
For this section, we are tasked to make a 10 x 10 ndarray of containing the squares of the first 100 positive integers and save the results as div_by_3.npy
1. I started by importing the NumPy library using import
```python
import numpy as np
```
2. Then I generated the square (i**2) of each integer from 1 to 100, and converted the list into a NumPy array
```python
A = np.array([i**2 for i in range(1,101)])
```
3. Then I reshaped the array into a 10×10 array using .reshape()
```python
A.reshape(10,10)
```
4. Then I used boolean indexing to select elements divisible by 3 then checks if the remainder is equal to zero
```python
divisible_by_3 = A[A%3 == 0]
```
5. Then I saved the filtered array to a .npy file called diy_by_3.npy
```python
np.save('diy_by_3', divisible_by_3)
```
6. Finally, I printed the array containing only elements divisible by 3
```python
print (divisible_by_3)
```
