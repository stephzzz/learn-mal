

```python
import numpy
```


```python
numpy.__version__
```




    '1.14.0'




```python
import numpy as np
```


```python
np.__version__
```




    '1.14.0'



## Python List的特點


```python
L= [i for i in range(9)]
L
```




    [0, 1, 2, 3, 4, 5, 6, 7, 8]




```python
L[5]
```




    5




```python
import array
```


```python
arr = array.array("i", [i for i in range(10)])
```


```python
arr
```




    array('i', [0, 1, 2, 3, 4, 5, 6, 7, 8, 9])




```python
arr[5]
```




    5




```python
arr[5] = 100
```


```python
arr
```




    array('i', [0, 1, 2, 3, 4, 100, 6, 7, 8, 9])




```python
arr[5] = "ls"
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-15-dd9b3726db6a> in <module>()
    ----> 1 arr[5] = "ls"
    

    TypeError: an integer is required (got type str)


## numpy.array


```python
nparr = np.array([i for i in range(10)])
```


```python
nparr
```




    array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])




```python
nparr[5]=100
nparr
```




    array([  0,   1,   2,   3,   4, 100,   6,   7,   8,   9])




```python
nparr[5] = "1123"
nparr
```




    array([   0,    1,    2,    3,    4, 1123,    6,    7,    8,    9])




```python
nparr[5] = "a"
nparr
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-20-db3c7ade07f7> in <module>()
    ----> 1 nparr[5] = "a"
          2 nparr
    

    ValueError: invalid literal for int() with base 10: 'a'



```python
nparr.dtype
```




    dtype('int32')




```python
nparr=5.0
nparr
```




    5.0




```python
nparr = np.array([i for i in range(10)])
nparr[5] = 5.0
```


```python
nparr
```




    array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])




```python
nparr2 = np.array([1,2,3.0])
```


```python
nparr2.dtype
```




    dtype('float64')



## 其他創建numpy.array的方法


```python
np.zeros(10)
```




    array([0., 0., 0., 0., 0., 0., 0., 0., 0., 0.])




```python
np.zeros(10).dtype
```




    dtype('float64')




```python
np.zeros(10, dtype=int)
```




    array([0, 0, 0, 0, 0, 0, 0, 0, 0, 0])




```python
np.zeros((3,5))
```




    array([[0., 0., 0., 0., 0.],
           [0., 0., 0., 0., 0.],
           [0., 0., 0., 0., 0.]])




```python
np.ones(10)
```




    array([1., 1., 1., 1., 1., 1., 1., 1., 1., 1.])




```python
np.ones((3,5))
```




    array([[1., 1., 1., 1., 1.],
           [1., 1., 1., 1., 1.],
           [1., 1., 1., 1., 1.]])




```python
np.ones((3,5), dtype=int)
```




    array([[1, 1, 1, 1, 1],
           [1, 1, 1, 1, 1],
           [1, 1, 1, 1, 1]])




```python
np.full((3, 5), 66)
```




    array([[66, 66, 66, 66, 66],
           [66, 66, 66, 66, 66],
           [66, 66, 66, 66, 66]])




```python
np.full((3, 5), 66.0)
```




    array([[66., 66., 66., 66., 66.],
           [66., 66., 66., 66., 66.],
           [66., 66., 66., 66., 66.]])




```python
np.full(fill_value=12, shape=10)
```




    array([12, 12, 12, 12, 12, 12, 12, 12, 12, 12])



## arange


```python
[i for i in range(10)]
```




    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]




```python
np.arange(10)
```




    array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])




```python
np.arange(0,20,2)
```




    array([ 0,  2,  4,  6,  8, 10, 12, 14, 16, 18])




```python
np.arange(0,10,0.2)
```




    array([0. , 0.2, 0.4, 0.6, 0.8, 1. , 1.2, 1.4, 1.6, 1.8, 2. , 2.2, 2.4,
           2.6, 2.8, 3. , 3.2, 3.4, 3.6, 3.8, 4. , 4.2, 4.4, 4.6, 4.8, 5. ,
           5.2, 5.4, 5.6, 5.8, 6. , 6.2, 6.4, 6.6, 6.8, 7. , 7.2, 7.4, 7.6,
           7.8, 8. , 8.2, 8.4, 8.6, 8.8, 9. , 9.2, 9.4, 9.6, 9.8])



## linspace等差數列


```python
np.linspace(0,20,10)
```




    array([ 0.        ,  2.22222222,  4.44444444,  6.66666667,  8.88888889,
           11.11111111, 13.33333333, 15.55555556, 17.77777778, 20.        ])




```python
np.linspace(0,20,11)
```




    array([ 0.,  2.,  4.,  6.,  8., 10., 12., 14., 16., 18., 20.])



## random


```python
np.random.randint(0,10)
```




    6




```python
np.random.randint(0,10,10)

```




    array([4, 4, 0, 0, 3, 8, 1, 1, 1, 9])



#### 不同於linspance,random的區間是前闭后开的


```python
np.random.randint(0,1,10)
```




    array([0, 0, 0, 0, 0, 0, 0, 0, 0, 0])



`pip install numpy`
