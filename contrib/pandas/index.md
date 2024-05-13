# List of sections

* [Basic Mathematics](#BasicMaths)
   * [What is a Matrix?](#Matrix-Intro)
   * [Scalars and Vectors](#Scalars-Vectors)

# Basic Mathematics
## What is a Matrix?
A matrix is a collection of numbers ordered in rows and columns. Here is one.

<body>
    <table>
        <tr>
            <td>1</td>
            <td>2</td>
            <td>3</td>
        </tr>
        <tr>
            <td>4</td>
            <td>5</td>
            <td>6</td>
        </tr>
        <tr>
            <td>7</td>
            <td>8</td>
            <td>9</td>
        </tr>
    </table>
</body>


A matrix is generally written within square brackets[]. The dimensions of a matrix is represented by (Number of rows X Number of columns).The dimensions of the above matrix is 3x3.

Matrices are the main characters in mathematical operations like addition, subtraction etc..especially those used in Pandas and NumPy. They can contain only numbers, symbols or expressions.

In order to refer to a particular element in the matrix we denote it by : 
A<sub>ij</sub>

where i represents the ith row and j represents the jth column of the matrix.

## Scalars and Vectors
### Scalars
There exists specific cases of matrices which are also widely used.

A matrix with only one row and column i.e. containing only one element is commonly referred to as a scalar.

The numbers [12] ; [-5] ; [0] ; [3.14] all represent scalars. Scalars have 0 dimensions.

### Vectors
Vectors are objects with 1 dimension. They sit somewhere between scalars and matrices. They can also be referred to as one dimensional matrices

[1 3 5] represents a vector with dimension 1x3.

A vector is the simplest linear algebraic object.A matrix can be refered to as a collection of vectors

Vectors are broadly classified into 2 types:
- Row Vectors: Is of the form 1 x n where n refers to the number of columns the vector has. 
- Column Vectors: Is of the form m x 1 where m refers to the number of rows the vector has.

m or n are also called as the length of the column and row vector respectively.

## Arrays in Python

To understand arrays first let us start by declaring scalars, vectors and matrices in Python.

First we need to import numpy. We do so by importing it as 'np' as it provides better readability, namespace clarity and also aligns with the community guidelines.

```
import numpy as np
```
Next up, we declare scalars as,
```
s = 5
```



Now we declare a vector,
```python
v = np.array([5,-2,4])
```
On printing v we get the following output,
```python
array([5,-2,4])
```
By default, a vector is declared as a **'row vector'**.

Finally, we declare matrices,
```python
m=np.array([[5,12,6],[-3,0,14]])
```
On printing m we get,
```python
array([[5,12,6],
        [-3,0,14]])
```
> The type() function is used to return the data type of a given variable.

* The type(s) will return 'int'.

* The type(v) will return 'numpy.ndarray' which represents a **n-dimensional array**, since it is a 1 dimensional array.
 
 * The type(m) will also return 'numpy.ndarray' since it is a 2-dimensional array.

These are some ways in which arrays are useful in python.

> The shape() function is used to return the shape of a given variable.

* m.shape() returns (2,3) since we are dealing with a (2,3) matrix.

* v.shape() returns(3,) indicates it has only one dimensional or that it stores 3 elements in order.

* However, 'int' objects do not have shape and therefore s.shape() gives an error.

## What is a Tensor?
A Tensor can be thought of as a collection of matrices. It has dimensions k x m x n.
**NOTE:** Scalars, vectors and matrices are also tensors of rank 0,1,2 respectively.

Tensors can be stored in ndarrays.

Let's create a tensor with 2 matrices,
```python
m1=np.array([[5,12,6],[-3,0,14]])
m2=np.array([[2,1,8],[-6,2,0]])
t=np.array([m1,m2])
```
Upon printing t we get,
```python
array([[[5,12,6],
        [-3,0,14]],
  
        [[2,1,8],
        [-6,2,0]]])
```
If we check it's shape, we see that is is a **(2,2,3)** object.

If we want to manually create a tensor we write,
```python
t=np.array([[[5,12,6], [-3,0,14]],[[2,1,8], [-6,2,0]]])
```
 ## Addition and Subtraction in Matrices

 ### Addition
 For 2 matrices to be added to one another they must have **same dimensions**.

 If we have 2 matrices say,

```python
A=np.array([[5,12,6],[-3,0,14]])
B=np.array([[2,1,8],[-6,2,0]])
C= A+B
  ```
The element at position A<sub>ij</sub> gets added to the element at position B<sub>ij</sub>. It's that simple!
The above input will give the resultant C as:
```python
array([[7,13,14],
        [-9,2,14]])
```
### Subtraction

As we know, subtraction is a type of addition, the same rules apply here.

 If we have 2 matrices say,

```python
A=np.array([[5,12,6],[-3,0,14]])
B=np.array([[2,1,8],[-6,2,0]])
C= A-B
  ```

The element at position B<sub>ij</sub> gets subtracted from the element at position A<sub>ij</sub>.
The above input will give the resultant C as:
```python
array([[3,11,-2],
        [3,-2,14]])
```
Similarly the same operations can be done with **floating point numbers** as well.

In a similar fashion, we can add  or subtract vectors as well with the condition that they must be of the **same length**.
```python
A=np.array([1,2,3,4,5])
B=np.array([6,7,8,9,10])
C= A+B
  ```
The result is a vector of length 5 with C as,
```python
array([7,9,11,13,15])
```
 ### Addition of scalars with vectors & matrices

 Scalars show unique behaviour when added to matrices or vectors.

 To demonstrate their behaviour, let's use an example,
 Let's declare a matrix,

```python
A=np.array([[5,12,6],[-3,0,14]])
A+1
```
We see that if we perform the above function, i.e. add scalar 1 to the matrix A we get the output,
```python
array([[6,13,7],[-2,1,15]])
```
We see that the scalar is added to the matrix elementwise, i.e. each element gets incremented by 1.

**The same applies to vectors as well.**

Mathematically, it is not allowed as the shape of scalars are different from vectors or matrices but while programming in Python it works.

## Transpose of Matrices & Vectors
### Transposing Vectors

If X is the vector, then the transpose of the vector is represented as X<sup>T</sup>. It changes a vector of dimension n x 1 into a vector of dimension 1 x n, i.e. a row vector to a column vector and vice versa.

> * The values are not changing or transforming ; only their position is.
> * Transposing the same vector (object) twice yields the initial vector (object)
