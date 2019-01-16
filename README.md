# Quiz01
Quiz 01 Date: June 11, 2018
'''
Christopher Mavor
Math 4330
Quiz 01
June 11th, 2018
'''
def matVec(matrix, vector):
  '''
This function takes a matrix and a vector as its arguments. It then updates each element of the matrix by multiplying it by the vector corresponding value before returning the now updated vector. 

Input values must be in matrix = m*n and vector in 1*n.
  '''
  A = [ ]
  sizematrix = len(matrix[0])
  sizevector = len(vector)
  # Assigning A as the empty matix value to store the results in. The size values are determining the size of the input values.
  if len(matrix) == len(matrix[0]) and len(matrix) == 1:
   print("Error in matrix sizing")

  if sizematrix == sizevector:
    # using this if condition to determine if matrix vector multiplication is capable.
    for i in range(len(matrix)):
      #this is determining how many rows there are in the matrix input to separate the opperations by each row of the matrix.
      rowx = [ ]
      # empty row vector to store the multiplication opperation of each row in.
      for j in range(len(matrix[i])):
       rowx.append(vector[j]*matrix[i][j])
       #opperation of vector elements multiplying bye each matrix row element.    
      rowx=sum(rowx)
      # summing the itemized multiplication after being placed in a list format.
      A.append(rowx)
      # sending the results from each row into the matrix
    return A
  else:
    return print("Error on matrix size. Make sure input values of matrix have the same number of columns as the vector.")

# These are test variables being initialized to test the function scalarVec.

testMatrix01 = 1
testMatrix02 = [[1,1,1],[2,2,2],[3,3,3]]
testMatrix03 = 'this is a test'

testVector01 = [1, 2, 3]
testVector02 = [1,1,1]
testVector03 = True

# These are test cases for the function matVec. All but one of the tests should be commented out at a time so that we can see how each pair of inputs effects the output. 

#print(matVec(testMatrix01,testVector01))
print(matVec(testMatrix02,testVector02))
#print(matVec(testMatrix03,testVector03))
a=1
