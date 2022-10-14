
# numpy

* [02-numpy.ipynb](notebooks/02-numpy.ipynb)
  * Practice indexing a multi-dimensional numpy array
* [02.00 introduction to numpy ](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/02.00-Introduction-to-NumPy.ipynb)
  * Creating arrays from Python lists
  * Creating arrays from scratch
* [02.01 understanding data types](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/02.01-Understanding-Data-Types.ipynb)
  * the standard python implementation is written in C 
  * every python object is actually a C structure
  * lists are mutable containers for python objects
  ```
  L3 = [True, "2", 3.0, 4]
  [type(item) for item in L3]
  ```
  * built-in `array`s provide efficient storage objects of uniform type
  * numpy arrays add efficient operations to built-in arrays -- this is a big deal
* [02.02 basics of numpy arrays](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/02.02-The-Basics-Of-NumPy-Arrays.ipynb)
  * there's more to numpy than 2-D arrays -- array creation with random number generator
  * dtype attribute -- datatype of the array
  * array indexing and slicing
  * multi-dimensional subarrays
  * subarrays as no-copy views!!
  * creating copies of arrays
  * reshaping arrays
  * array concatenation and splitting
* Other sections have a lot more important information
  * vectorizing
  * sorting
  * performance
