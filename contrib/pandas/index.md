# List of sections

* [Basic Mathematics](#BasicMaths)
   * [What is a Matrix?](#Matrix-Intro)
   * [Scalars and Vectors](#Scalars-Vectors)

# Basic Mathematics
## What is a Matrix?
A matrix is a collection of numbers ordered in rows and columns. Here is one.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
   
</head>
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
</html>

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


