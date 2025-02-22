{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 1,
   "metadata": {},
   "outputs": [],
   "source": [
    "import numpy as np"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Datatypes & Attributes"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([1, 2, 3])"
      ]
     },
     "execution_count": 2,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# NumPy's main datatype is ndarray\n",
    "a1 = np.array([1, 2, 3])\n",
    "a1"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "numpy.ndarray"
      ]
     },
     "execution_count": 3,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "type(a1)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "metadata": {},
   "outputs": [],
   "source": [
    "a2 = np.array([[1, 2.0, 3.3], [4, 5, 6.5]])\n",
    "\n",
    "a3 = np.array([[[1, 2, 3],\n",
    "               [4, 5, 6],\n",
    "               [7, 8, 9]],\n",
    "               [[10, 11, 12],\n",
    "               [13, 14, 15],\n",
    "               [16, 17, 18]]])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1. , 2. , 3.3],\n",
       "       [4. , 5. , 6.5]])"
      ]
     },
     "execution_count": 5,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[[ 1,  2,  3],\n",
       "        [ 4,  5,  6],\n",
       "        [ 7,  8,  9]],\n",
       "\n",
       "       [[10, 11, 12],\n",
       "        [13, 14, 15],\n",
       "        [16, 17, 18]]])"
      ]
     },
     "execution_count": 6,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a3"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(3,)"
      ]
     },
     "execution_count": 7,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(2, 3)"
      ]
     },
     "execution_count": 8,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a2.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(2, 3, 3)"
      ]
     },
     "execution_count": 9,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a3.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(1, 2, 3)"
      ]
     },
     "execution_count": 10,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1.ndim, a2.ndim, a3.ndim"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 12,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(dtype('int64'), dtype('float64'), dtype('int64'))"
      ]
     },
     "execution_count": 12,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1.dtype, a2.dtype, a3.dtype"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 13,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(3, 6, 18)"
      ]
     },
     "execution_count": 13,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1.size, a2.size, a3.size"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 14,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(numpy.ndarray, numpy.ndarray, numpy.ndarray)"
      ]
     },
     "execution_count": 14,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "type(a1), type(a2), type(a3)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 15,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>0</th>\n",
       "      <th>1</th>\n",
       "      <th>2</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>1.0</td>\n",
       "      <td>2.0</td>\n",
       "      <td>3.3</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>4.0</td>\n",
       "      <td>5.0</td>\n",
       "      <td>6.5</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "     0    1    2\n",
       "0  1.0  2.0  3.3\n",
       "1  4.0  5.0  6.5"
      ]
     },
     "execution_count": 15,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Create a DataFrame from a NumPy array\n",
    "import pandas as pd\n",
    "\n",
    "df = pd.DataFrame(a2)\n",
    "df"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 17,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([1, 2, 3])"
      ]
     },
     "execution_count": 17,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "sample_array = np.array([1, 2, 3])\n",
    "sample_array"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 18,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "dtype('int64')"
      ]
     },
     "execution_count": 18,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "sample_array.dtype"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 19,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1., 1., 1.],\n",
       "       [1., 1., 1.]])"
      ]
     },
     "execution_count": 19,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "ones = np.ones((2, 3))\n",
    "ones"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 20,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "dtype('float64')"
      ]
     },
     "execution_count": 20,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "ones.dtype"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 21,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "numpy.ndarray"
      ]
     },
     "execution_count": 21,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "type(ones)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 23,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[0., 0., 0.],\n",
       "       [0., 0., 0.]])"
      ]
     },
     "execution_count": 23,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "zeros = np.zeros((2, 3))\n",
    "zeros"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 24,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([0, 2, 4, 6, 8])"
      ]
     },
     "execution_count": 24,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "range_array = np.arange(0, 10, 2)\n",
    "range_array"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 28,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[5, 4, 7, 5, 9],\n",
       "       [3, 8, 5, 6, 6],\n",
       "       [7, 6, 3, 6, 9]])"
      ]
     },
     "execution_count": 28,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "random_array = np.random.randint(0, 10, size=(3, 5))\n",
    "random_array"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 29,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "15"
      ]
     },
     "execution_count": 29,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "random_array.size"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 30,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(3, 5)"
      ]
     },
     "execution_count": 30,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "random_array.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 31,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[0.67093844, 0.77173084, 0.98622059],\n",
       "       [0.00625919, 0.86436955, 0.54106733],\n",
       "       [0.71498498, 0.58036144, 0.71878739],\n",
       "       [0.6300464 , 0.8336507 , 0.85038884],\n",
       "       [0.26521107, 0.69955084, 0.07618093]])"
      ]
     },
     "execution_count": 31,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "random_array_2 = np.random.random((5, 3))\n",
    "random_array_2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 32,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(5, 3)"
      ]
     },
     "execution_count": 32,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "random_array_2.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 33,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[0.83749061, 0.25520532, 0.37797197],\n",
       "       [0.7060974 , 0.87374275, 0.41201583],\n",
       "       [0.42143342, 0.45152025, 0.91165354],\n",
       "       [0.98544473, 0.996407  , 0.18046736],\n",
       "       [0.63849459, 0.71129745, 0.37717359]])"
      ]
     },
     "execution_count": 33,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "random_array_3 = np.random.rand(5, 3)\n",
    "random_array_3"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 40,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[5, 0, 3],\n",
       "       [3, 7, 9],\n",
       "       [3, 5, 2],\n",
       "       [4, 7, 6],\n",
       "       [8, 8, 1]])"
      ]
     },
     "execution_count": 40,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Pseudo-random numbers\n",
    "np.random.seed(seed=0)\n",
    "random_array_4 = np.random.randint(10, size=(5, 3))\n",
    "random_array_4"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 38,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(5, 3)"
      ]
     },
     "execution_count": 38,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "random_array_4.shape"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 3. Viewing Arrays and Matrices"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 41,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])"
      ]
     },
     "execution_count": 41,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.unique(random_array_4)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 42,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([1, 2, 3])"
      ]
     },
     "execution_count": 42,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 43,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1. , 2. , 3.3],\n",
       "       [4. , 5. , 6.5]])"
      ]
     },
     "execution_count": 43,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 44,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[[ 1,  2,  3],\n",
       "        [ 4,  5,  6],\n",
       "        [ 7,  8,  9]],\n",
       "\n",
       "       [[10, 11, 12],\n",
       "        [13, 14, 15],\n",
       "        [16, 17, 18]]])"
      ]
     },
     "execution_count": 44,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a3"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 45,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "1"
      ]
     },
     "execution_count": 45,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1[0]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 46,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([1. , 2. , 3.3])"
      ]
     },
     "execution_count": 46,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a2[0]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 47,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(2, 3, 3)"
      ]
     },
     "execution_count": 47,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a3.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 48,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1, 2, 3],\n",
       "       [4, 5, 6],\n",
       "       [7, 8, 9]])"
      ]
     },
     "execution_count": 48,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a3[0]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 49,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[[ 1,  2,  3],\n",
       "        [ 4,  5,  6],\n",
       "        [ 7,  8,  9]],\n",
       "\n",
       "       [[10, 11, 12],\n",
       "        [13, 14, 15],\n",
       "        [16, 17, 18]]])"
      ]
     },
     "execution_count": 49,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a3"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 50,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[[ 1,  2],\n",
       "        [ 4,  5]],\n",
       "\n",
       "       [[10, 11],\n",
       "        [13, 14]]])"
      ]
     },
     "execution_count": 50,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a3[:2, :2, :2]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 52,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[[[8, 8, 2, 3, 2],\n",
       "         [0, 8, 8, 3, 8],\n",
       "         [2, 8, 4, 3, 0],\n",
       "         [4, 3, 6, 9, 8]],\n",
       "\n",
       "        [[0, 8, 5, 9, 0],\n",
       "         [9, 6, 5, 3, 1],\n",
       "         [8, 0, 4, 9, 6],\n",
       "         [5, 7, 8, 8, 9]],\n",
       "\n",
       "        [[2, 8, 6, 6, 9],\n",
       "         [1, 6, 8, 8, 3],\n",
       "         [2, 3, 6, 3, 6],\n",
       "         [5, 7, 0, 8, 4]]],\n",
       "\n",
       "\n",
       "       [[[6, 5, 8, 2, 3],\n",
       "         [9, 7, 5, 3, 4],\n",
       "         [5, 3, 3, 7, 9],\n",
       "         [9, 9, 7, 3, 2]],\n",
       "\n",
       "        [[3, 9, 7, 7, 5],\n",
       "         [1, 2, 2, 8, 1],\n",
       "         [5, 8, 4, 0, 2],\n",
       "         [5, 5, 0, 8, 1]],\n",
       "\n",
       "        [[1, 0, 3, 8, 8],\n",
       "         [4, 4, 0, 9, 3],\n",
       "         [7, 3, 2, 1, 1],\n",
       "         [2, 1, 4, 2, 5]]]])"
      ]
     },
     "execution_count": 52,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a4 = np.random.randint(10, size=(2, 3, 4, 5))\n",
    "a4"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 54,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "((2, 3, 4, 5), 4)"
      ]
     },
     "execution_count": 54,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a4.shape, a4.ndim"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 56,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[[[8, 8],\n",
       "         [0, 8],\n",
       "         [2, 8],\n",
       "         [4, 3]],\n",
       "\n",
       "        [[0, 8],\n",
       "         [9, 6],\n",
       "         [8, 0],\n",
       "         [5, 7]],\n",
       "\n",
       "        [[2, 8],\n",
       "         [1, 6],\n",
       "         [2, 3],\n",
       "         [5, 7]]],\n",
       "\n",
       "\n",
       "       [[[6, 5],\n",
       "         [9, 7],\n",
       "         [5, 3],\n",
       "         [9, 9]],\n",
       "\n",
       "        [[3, 9],\n",
       "         [1, 2],\n",
       "         [5, 8],\n",
       "         [5, 5]],\n",
       "\n",
       "        [[1, 0],\n",
       "         [4, 4],\n",
       "         [7, 3],\n",
       "         [2, 1]]]])"
      ]
     },
     "execution_count": 56,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Get the first 2 numbers of the innermost array\n",
    "a4[:, :, :, :2]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 4. Manipulating & Comparing Arrays"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Arithmetic"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 57,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([1, 2, 3])"
      ]
     },
     "execution_count": 57,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 58,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([1., 1., 1.])"
      ]
     },
     "execution_count": 58,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "ones = np.ones(3)\n",
    "ones"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 59,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([2., 3., 4.])"
      ]
     },
     "execution_count": 59,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1 + ones"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 60,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([0., 1., 2.])"
      ]
     },
     "execution_count": 60,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1 - ones"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 61,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([1., 2., 3.])"
      ]
     },
     "execution_count": 61,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1 * ones"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 62,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1. , 2. , 3.3],\n",
       "       [4. , 5. , 6.5]])"
      ]
     },
     "execution_count": 62,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 63,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[ 1. ,  4. ,  9.9],\n",
       "       [ 4. , 10. , 19.5]])"
      ]
     },
     "execution_count": 63,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1 * a2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 64,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[[ 1,  2,  3],\n",
       "        [ 4,  5,  6],\n",
       "        [ 7,  8,  9]],\n",
       "\n",
       "       [[10, 11, 12],\n",
       "        [13, 14, 15],\n",
       "        [16, 17, 18]]])"
      ]
     },
     "execution_count": 64,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a3"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 65,
   "metadata": {},
   "outputs": [
    {
     "ename": "ValueError",
     "evalue": "operands could not be broadcast together with shapes (2,3) (2,3,3) ",
     "output_type": "error",
     "traceback": [
      "\u001b[0;31m---------------------------------------------------------------------------\u001b[0m",
      "\u001b[0;31mValueError\u001b[0m                                Traceback (most recent call last)",
      "\u001b[0;32m<ipython-input-65-37d8620f1b2c>\u001b[0m in \u001b[0;36m<module>\u001b[0;34m\u001b[0m\n\u001b[0;32m----> 1\u001b[0;31m \u001b[0ma2\u001b[0m \u001b[0;34m*\u001b[0m \u001b[0ma3\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0m",
      "\u001b[0;31mValueError\u001b[0m: operands could not be broadcast together with shapes (2,3) (2,3,3) "
     ]
    }
   ],
   "source": [
    "a2 * a3"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 66,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([1., 2., 3.])"
      ]
     },
     "execution_count": 66,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1 / ones"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 67,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1., 1., 1.],\n",
       "       [4., 2., 2.]])"
      ]
     },
     "execution_count": 67,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Floor division removes the decimals (rounds down)\n",
    "a2 // a1"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 68,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[ 1.  ,  4.  , 10.89],\n",
       "       [16.  , 25.  , 42.25]])"
      ]
     },
     "execution_count": 68,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a2 ** 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 69,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[ 1.  ,  4.  , 10.89],\n",
       "       [16.  , 25.  , 42.25]])"
      ]
     },
     "execution_count": 69,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.square(a2)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 70,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([2., 3., 4.])"
      ]
     },
     "execution_count": 70,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.add(a1, ones)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 71,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([1, 0, 1])"
      ]
     },
     "execution_count": 71,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1 % 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 72,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1. , 0. , 1.3],\n",
       "       [0. , 1. , 0.5]])"
      ]
     },
     "execution_count": 72,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a2 % 2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 73,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([ 2.71828183,  7.3890561 , 20.08553692])"
      ]
     },
     "execution_count": 73,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.exp(a1)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 74,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([0.        , 0.69314718, 1.09861229])"
      ]
     },
     "execution_count": 74,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.log(a1)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Aggregation\n",
    "aggregation = performing the same operation on a number of things"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 75,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "list"
      ]
     },
     "execution_count": 75,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "listy_list = [1, 2, 3]\n",
    "type(listy_list)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 76,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "6"
      ]
     },
     "execution_count": 76,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "sum(listy_list)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 78,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "6"
      ]
     },
     "execution_count": 78,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "sum(a1)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 79,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "6"
      ]
     },
     "execution_count": 79,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.sum(a1)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Use Python's methods (e.g. `sum()`) on Python datatypes and use NumPy's methods on NumPy arrays (e.g. `np.sum()`)."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 80,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "100000"
      ]
     },
     "execution_count": 80,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Creating a massive NumPy array\n",
    "massive_array = np.random.random(100000)\n",
    "massive_array.size"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 81,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([0.21874937, 0.56957353, 0.45210904, 0.97023668, 0.68054469,\n",
       "       0.08529557, 0.05641833, 0.4878377 , 0.88100456, 0.97640439])"
      ]
     },
     "execution_count": 81,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "massive_array[:10]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 84,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "15.6 ms ± 327 µs per loop (mean ± std. dev. of 7 runs, 100 loops each)\n",
      "34.3 µs ± 977 ns per loop (mean ± std. dev. of 7 runs, 10000 loops each)\n"
     ]
    }
   ],
   "source": [
    "%timeit sum(massive_array) # Python's sum()\n",
    "%timeit np.sum(massive_array) # NumPy's np.sum()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 85,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "3.6333333333333333"
      ]
     },
     "execution_count": 85,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.mean(a2)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 86,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "6.5"
      ]
     },
     "execution_count": 86,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.max(a2)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 87,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "1.0"
      ]
     },
     "execution_count": 87,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.min(a2)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 88,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "1.8226964152656422"
      ]
     },
     "execution_count": 88,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# standard deviation = measure of how spread out a group of numbers is from the mean\n",
    "np.std(a2)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 89,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "3.3222222222222224"
      ]
     },
     "execution_count": 89,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Variance = measure of avg degree to which each number is different than the mean\n",
    "np.var(a2)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 90,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "1.8226964152656422"
      ]
     },
     "execution_count": 90,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Standard deviation = square root of variance\n",
    "np.sqrt(np.var(a2))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 91,
   "metadata": {},
   "outputs": [],
   "source": [
    "# Demo of std and var\n",
    "high_var_array = np.array([1, 100, 200, 300, 4000, 5000])\n",
    "low_var_array = np.array([2, 4, 6, 8, 10])"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 92,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(4296133.472222221, 8.0)"
      ]
     },
     "execution_count": 92,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.var(high_var_array), np.var(low_var_array)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 93,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(2072.711623024829, 2.8284271247461903)"
      ]
     },
     "execution_count": 93,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.std(high_var_array), np.std(low_var_array)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 94,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(1600.1666666666667, 6.0)"
      ]
     },
     "execution_count": 94,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.mean(high_var_array), np.mean(low_var_array)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 95,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "%matplotlib inline\n",
    "import matplotlib.pyplot as plt\n",
    "plt.hist(high_var_array)\n",
    "plt.show()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 96,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(array([1., 0., 1., 0., 0., 1., 0., 1., 0., 1.]),\n",
       " array([ 2. ,  2.8,  3.6,  4.4,  5.2,  6. ,  6.8,  7.6,  8.4,  9.2, 10. ]),\n",
       " <a list of 10 Patch objects>)"
      ]
     },
     "execution_count": 96,
     "metadata": {},
     "output_type": "execute_result"
    },
    {
     "data": {
      "image/png": "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\n",
      "text/plain": [
       "<Figure size 432x288 with 1 Axes>"
      ]
     },
     "metadata": {
      "needs_background": "light"
     },
     "output_type": "display_data"
    }
   ],
   "source": [
    "plt.hist(low_var_array)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Reshaping & Transposing"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 97,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1. , 2. , 3.3],\n",
       "       [4. , 5. , 6.5]])"
      ]
     },
     "execution_count": 97,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 98,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(2, 3)"
      ]
     },
     "execution_count": 98,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a2.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 99,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(2, 3, 3)"
      ]
     },
     "execution_count": 99,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a3.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 100,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[[ 1,  2,  3],\n",
       "        [ 4,  5,  6],\n",
       "        [ 7,  8,  9]],\n",
       "\n",
       "       [[10, 11, 12],\n",
       "        [13, 14, 15],\n",
       "        [16, 17, 18]]])"
      ]
     },
     "execution_count": 100,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a3"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 101,
   "metadata": {},
   "outputs": [
    {
     "ename": "ValueError",
     "evalue": "operands could not be broadcast together with shapes (2,3) (2,3,3) ",
     "output_type": "error",
     "traceback": [
      "\u001b[0;31m---------------------------------------------------------------------------\u001b[0m",
      "\u001b[0;31mValueError\u001b[0m                                Traceback (most recent call last)",
      "\u001b[0;32m<ipython-input-101-37d8620f1b2c>\u001b[0m in \u001b[0;36m<module>\u001b[0;34m\u001b[0m\n\u001b[0;32m----> 1\u001b[0;31m \u001b[0ma2\u001b[0m \u001b[0;34m*\u001b[0m \u001b[0ma3\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0m",
      "\u001b[0;31mValueError\u001b[0m: operands could not be broadcast together with shapes (2,3) (2,3,3) "
     ]
    }
   ],
   "source": [
    "a2 * a3"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 106,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[[1. ],\n",
       "        [2. ],\n",
       "        [3.3]],\n",
       "\n",
       "       [[4. ],\n",
       "        [5. ],\n",
       "        [6.5]]])"
      ]
     },
     "execution_count": 106,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a2_reshape = a2.reshape(2, 3, 1)\n",
    "a2_reshape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 107,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(2, 3, 1)"
      ]
     },
     "execution_count": 107,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a2_reshape.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 108,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[[  1. ,   2. ,   3. ],\n",
       "        [  8. ,  10. ,  12. ],\n",
       "        [ 23.1,  26.4,  29.7]],\n",
       "\n",
       "       [[ 40. ,  44. ,  48. ],\n",
       "        [ 65. ,  70. ,  75. ],\n",
       "        [104. , 110.5, 117. ]]])"
      ]
     },
     "execution_count": 108,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a2_reshape * a3"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 109,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1. , 2. , 3.3],\n",
       "       [4. , 5. , 6.5]])"
      ]
     },
     "execution_count": 109,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 110,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1. , 4. ],\n",
       "       [2. , 5. ],\n",
       "       [3.3, 6.5]])"
      ]
     },
     "execution_count": 110,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Transpose = switches the axis\n",
    "a2.T"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 111,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[[ 1,  2,  3],\n",
       "        [ 4,  5,  6],\n",
       "        [ 7,  8,  9]],\n",
       "\n",
       "       [[10, 11, 12],\n",
       "        [13, 14, 15],\n",
       "        [16, 17, 18]]])"
      ]
     },
     "execution_count": 111,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a3"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 112,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(2, 3, 3)"
      ]
     },
     "execution_count": 112,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a3.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 113,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(3, 3, 2)"
      ]
     },
     "execution_count": 113,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a3.T.shape"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Dot Product"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 114,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[5, 0, 3],\n",
       "       [3, 7, 9],\n",
       "       [3, 5, 2],\n",
       "       [4, 7, 6],\n",
       "       [8, 8, 1]])"
      ]
     },
     "execution_count": 114,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.random.seed(0)\n",
    "\n",
    "mat1 = np.random.randint(10, size=(5, 3))\n",
    "mat2 = np.random.randint(10, size=(5, 3))\n",
    "\n",
    "mat1"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 115,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[6, 7, 7],\n",
       "       [8, 1, 5],\n",
       "       [9, 8, 9],\n",
       "       [4, 3, 0],\n",
       "       [3, 5, 0]])"
      ]
     },
     "execution_count": 115,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "mat2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 116,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "((5, 3), (5, 3))"
      ]
     },
     "execution_count": 116,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "mat1.shape, mat2.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 117,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[30,  0, 21],\n",
       "       [24,  7, 45],\n",
       "       [27, 40, 18],\n",
       "       [16, 21,  0],\n",
       "       [24, 40,  0]])"
      ]
     },
     "execution_count": 117,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Element-wise multiplication (Hadamard product)\n",
    "mat1 * mat2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 118,
   "metadata": {},
   "outputs": [
    {
     "ename": "ValueError",
     "evalue": "shapes (5,3) and (5,3) not aligned: 3 (dim 1) != 5 (dim 0)",
     "output_type": "error",
     "traceback": [
      "\u001b[0;31m---------------------------------------------------------------------------\u001b[0m",
      "\u001b[0;31mValueError\u001b[0m                                Traceback (most recent call last)",
      "\u001b[0;32m<ipython-input-118-0da3c94cc631>\u001b[0m in \u001b[0;36m<module>\u001b[0;34m\u001b[0m\n\u001b[1;32m      1\u001b[0m \u001b[0;31m# Dot product\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0;32m----> 2\u001b[0;31m \u001b[0mnp\u001b[0m\u001b[0;34m.\u001b[0m\u001b[0mdot\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0mmat1\u001b[0m\u001b[0;34m,\u001b[0m \u001b[0mmat2\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0m",
      "\u001b[0;32m<__array_function__ internals>\u001b[0m in \u001b[0;36mdot\u001b[0;34m(*args, **kwargs)\u001b[0m\n",
      "\u001b[0;31mValueError\u001b[0m: shapes (5,3) and (5,3) not aligned: 3 (dim 1) != 5 (dim 0)"
     ]
    }
   ],
   "source": [
    "# Dot product\n",
    "np.dot(mat1, mat2)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 119,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[5, 3, 3, 4, 8],\n",
       "       [0, 7, 5, 7, 8],\n",
       "       [3, 9, 2, 6, 1]])"
      ]
     },
     "execution_count": 119,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Transpose mat1\n",
    "mat1.T"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 121,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "((5, 3), (3, 5))"
      ]
     },
     "execution_count": 121,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "mat1.shape, mat2.T.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 122,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[ 51,  55,  72,  20,  15],\n",
       "       [130,  76, 164,  33,  44],\n",
       "       [ 67,  39,  85,  27,  34],\n",
       "       [115,  69, 146,  37,  47],\n",
       "       [111,  77, 145,  56,  64]])"
      ]
     },
     "execution_count": 122,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "mat3 = np.dot(mat1, mat2.T)\n",
    "mat3"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 123,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(5, 5)"
      ]
     },
     "execution_count": 123,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "mat3.shape"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Dot Product Example (Nut Butter Sales)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 124,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[12, 15,  0],\n",
       "       [ 3,  3,  7],\n",
       "       [ 9, 19, 18],\n",
       "       [ 4,  6, 12],\n",
       "       [ 1,  6,  7]])"
      ]
     },
     "execution_count": 124,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.random.seed(0)\n",
    "# Number of jars sold\n",
    "sales_amounts = np.random.randint(20, size=(5, 3))\n",
    "sales_amounts"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 126,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Almond butter</th>\n",
       "      <th>Peanut butter</th>\n",
       "      <th>Cashew butter</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>Mon</th>\n",
       "      <td>12</td>\n",
       "      <td>15</td>\n",
       "      <td>0</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Tues</th>\n",
       "      <td>3</td>\n",
       "      <td>3</td>\n",
       "      <td>7</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Wed</th>\n",
       "      <td>9</td>\n",
       "      <td>19</td>\n",
       "      <td>18</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Thurs</th>\n",
       "      <td>4</td>\n",
       "      <td>6</td>\n",
       "      <td>12</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Fri</th>\n",
       "      <td>1</td>\n",
       "      <td>6</td>\n",
       "      <td>7</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "       Almond butter  Peanut butter  Cashew butter\n",
       "Mon               12             15              0\n",
       "Tues               3              3              7\n",
       "Wed                9             19             18\n",
       "Thurs              4              6             12\n",
       "Fri                1              6              7"
      ]
     },
     "execution_count": 126,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Create weekly_sales DataFrame\n",
    "weekly_sales = pd.DataFrame(sales_amounts,\n",
    "                           index=[\"Mon\", \"Tues\", \"Wed\", \"Thurs\", \"Fri\"],\n",
    "                           columns=[\"Almond butter\", \"Peanut butter\", \"Cashew butter\"])\n",
    "weekly_sales"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 127,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([10,  8, 12])"
      ]
     },
     "execution_count": 127,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Create prices array\n",
    "prices = np.array([10, 8, 12])\n",
    "prices"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 129,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Almond butter</th>\n",
       "      <th>Peanut butter</th>\n",
       "      <th>Cashew butter</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>Price</th>\n",
       "      <td>10</td>\n",
       "      <td>8</td>\n",
       "      <td>12</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "       Almond butter  Peanut butter  Cashew butter\n",
       "Price             10              8             12"
      ]
     },
     "execution_count": 129,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Create butter_prices DataFrame\n",
    "butter_prices = pd.DataFrame(prices.reshape(1, 3),\n",
    "                            index=[\"Price\"],\n",
    "                            columns=[\"Almond butter\", \"Peanut butter\", \"Cashew butter\"])\n",
    "butter_prices"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 130,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([10,  8, 12])"
      ]
     },
     "execution_count": 130,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "prices"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 131,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[12, 15,  0],\n",
       "       [ 3,  3,  7],\n",
       "       [ 9, 19, 18],\n",
       "       [ 4,  6, 12],\n",
       "       [ 1,  6,  7]])"
      ]
     },
     "execution_count": 131,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "sales_amounts"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 132,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([240, 138, 458, 232, 142])"
      ]
     },
     "execution_count": 132,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Shapes aren't aligned, lets transpose\n",
    "total_sales = prices.dot(sales_amounts.T)\n",
    "total_sales"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 133,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "((1, 3), (5, 3))"
      ]
     },
     "execution_count": 133,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# Create daily_sales\n",
    "butter_prices.shape, weekly_sales.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 134,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Mon</th>\n",
       "      <th>Tues</th>\n",
       "      <th>Wed</th>\n",
       "      <th>Thurs</th>\n",
       "      <th>Fri</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>Price</th>\n",
       "      <td>240</td>\n",
       "      <td>138</td>\n",
       "      <td>458</td>\n",
       "      <td>232</td>\n",
       "      <td>142</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "       Mon  Tues  Wed  Thurs  Fri\n",
       "Price  240   138  458    232  142"
      ]
     },
     "execution_count": 134,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "daily_sales = butter_prices.dot(weekly_sales.T)\n",
    "daily_sales"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 135,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>Almond butter</th>\n",
       "      <th>Peanut butter</th>\n",
       "      <th>Cashew butter</th>\n",
       "      <th>Total ($)</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>Mon</th>\n",
       "      <td>12</td>\n",
       "      <td>15</td>\n",
       "      <td>0</td>\n",
       "      <td>240</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Tues</th>\n",
       "      <td>3</td>\n",
       "      <td>3</td>\n",
       "      <td>7</td>\n",
       "      <td>138</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Wed</th>\n",
       "      <td>9</td>\n",
       "      <td>19</td>\n",
       "      <td>18</td>\n",
       "      <td>458</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Thurs</th>\n",
       "      <td>4</td>\n",
       "      <td>6</td>\n",
       "      <td>12</td>\n",
       "      <td>232</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Fri</th>\n",
       "      <td>1</td>\n",
       "      <td>6</td>\n",
       "      <td>7</td>\n",
       "      <td>142</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "       Almond butter  Peanut butter  Cashew butter  Total ($)\n",
       "Mon               12             15              0        240\n",
       "Tues               3              3              7        138\n",
       "Wed                9             19             18        458\n",
       "Thurs              4              6             12        232\n",
       "Fri                1              6              7        142"
      ]
     },
     "execution_count": 135,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "weekly_sales[\"Total ($)\"] = daily_sales.T\n",
    "weekly_sales"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Comparison Operators"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 136,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([1, 2, 3])"
      ]
     },
     "execution_count": 136,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 137,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1. , 2. , 3.3],\n",
       "       [4. , 5. , 6.5]])"
      ]
     },
     "execution_count": 137,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 138,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[False, False, False],\n",
       "       [False, False, False]])"
      ]
     },
     "execution_count": 138,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1 > a2"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 140,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[ True,  True, False],\n",
       "       [False, False, False]])"
      ]
     },
     "execution_count": 140,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "bool_array = a1 >= a2\n",
    "bool_array"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 141,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(numpy.ndarray, dtype('bool'))"
      ]
     },
     "execution_count": 141,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "type(bool_array), bool_array.dtype"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 142,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([False, False, False])"
      ]
     },
     "execution_count": 142,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1 > 5"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 143,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([ True,  True,  True])"
      ]
     },
     "execution_count": 143,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1 < 5"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 144,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([ True,  True,  True])"
      ]
     },
     "execution_count": 144,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1 == a1"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 145,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[ True,  True, False],\n",
       "       [False, False, False]])"
      ]
     },
     "execution_count": 145,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1 == a2"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 5. Sorting Arrays"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 146,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[7, 8, 1, 5, 9],\n",
       "       [8, 9, 4, 3, 0],\n",
       "       [3, 5, 0, 2, 3]])"
      ]
     },
     "execution_count": 146,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "random_array = np.random.randint(10, size=(3, 5))\n",
    "random_array"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 147,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(3, 5)"
      ]
     },
     "execution_count": 147,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "random_array.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 148,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[1, 5, 7, 8, 9],\n",
       "       [0, 3, 4, 8, 9],\n",
       "       [0, 2, 3, 3, 5]])"
      ]
     },
     "execution_count": 148,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.sort(random_array)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 149,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[2, 3, 0, 1, 4],\n",
       "       [4, 3, 2, 0, 1],\n",
       "       [2, 3, 0, 4, 1]])"
      ]
     },
     "execution_count": 149,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.argsort(random_array)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 150,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([1, 2, 3])"
      ]
     },
     "execution_count": 150,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "a1"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 151,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([0, 1, 2])"
      ]
     },
     "execution_count": 151,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.argsort(a1)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 152,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "0"
      ]
     },
     "execution_count": 152,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.argmin(a1)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 153,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "2"
      ]
     },
     "execution_count": 153,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.argmax(a1)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 154,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[7, 8, 1, 5, 9],\n",
       "       [8, 9, 4, 3, 0],\n",
       "       [3, 5, 0, 2, 3]])"
      ]
     },
     "execution_count": 154,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "random_array"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 156,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([1, 1, 1, 0, 0])"
      ]
     },
     "execution_count": 156,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.argmax(random_array, axis=0)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 157,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([4, 1, 1])"
      ]
     },
     "execution_count": 157,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "np.argmax(random_array, axis=1)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## 6. Practical Example - Turn Images Into NumPy Arrays"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<img src=\"images/panda.png\"/>"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 162,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "<class 'numpy.ndarray'>\n"
     ]
    }
   ],
   "source": [
    "# Turn an image into a NumPy array\n",
    "from matplotlib.image import imread\n",
    "\n",
    "panda = imread(\"images/panda.png\")\n",
    "print(type(panda))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 163,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(24465000, (2330, 3500, 3), 3)"
      ]
     },
     "execution_count": 163,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "panda.size, panda.shape, panda.ndim"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 164,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[[0.05490196, 0.10588235, 0.06666667],\n",
       "        [0.05490196, 0.10588235, 0.06666667],\n",
       "        [0.05490196, 0.10588235, 0.06666667],\n",
       "        ...,\n",
       "        [0.16470589, 0.12941177, 0.09411765],\n",
       "        [0.16470589, 0.12941177, 0.09411765],\n",
       "        [0.16470589, 0.12941177, 0.09411765]],\n",
       "\n",
       "       [[0.05490196, 0.10588235, 0.06666667],\n",
       "        [0.05490196, 0.10588235, 0.06666667],\n",
       "        [0.05490196, 0.10588235, 0.06666667],\n",
       "        ...,\n",
       "        [0.16470589, 0.12941177, 0.09411765],\n",
       "        [0.16470589, 0.12941177, 0.09411765],\n",
       "        [0.16470589, 0.12941177, 0.09411765]],\n",
       "\n",
       "       [[0.05490196, 0.10588235, 0.06666667],\n",
       "        [0.05490196, 0.10588235, 0.06666667],\n",
       "        [0.05490196, 0.10588235, 0.06666667],\n",
       "        ...,\n",
       "        [0.16470589, 0.12941177, 0.09411765],\n",
       "        [0.16470589, 0.12941177, 0.09411765],\n",
       "        [0.16470589, 0.12941177, 0.09411765]],\n",
       "\n",
       "       [[0.05490196, 0.10588235, 0.06666667],\n",
       "        [0.05490196, 0.10588235, 0.06666667],\n",
       "        [0.05490196, 0.10588235, 0.06666667],\n",
       "        ...,\n",
       "        [0.16862746, 0.13333334, 0.09803922],\n",
       "        [0.16862746, 0.13333334, 0.09803922],\n",
       "        [0.16862746, 0.13333334, 0.09803922]],\n",
       "\n",
       "       [[0.05490196, 0.10588235, 0.06666667],\n",
       "        [0.05490196, 0.10588235, 0.06666667],\n",
       "        [0.05490196, 0.10588235, 0.06666667],\n",
       "        ...,\n",
       "        [0.16862746, 0.13333334, 0.09803922],\n",
       "        [0.16862746, 0.13333334, 0.09803922],\n",
       "        [0.16862746, 0.13333334, 0.09803922]]], dtype=float32)"
      ]
     },
     "execution_count": 164,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "panda[:5]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<img src=\"images/car-photo.png\" />"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 165,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "<class 'numpy.ndarray'>\n"
     ]
    }
   ],
   "source": [
    "car = imread(\"images/car-photo.png\")\n",
    "print(type(car))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 166,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[[0.5019608 , 0.50980395, 0.4862745 , 1.        ],\n",
       "        [0.3372549 , 0.34509805, 0.30588236, 1.        ],\n",
       "        [0.20392157, 0.21568628, 0.14901961, 1.        ],\n",
       "        ...,\n",
       "        [0.64705884, 0.7058824 , 0.54901963, 1.        ],\n",
       "        [0.59607846, 0.63529414, 0.45882353, 1.        ],\n",
       "        [0.44705883, 0.47058824, 0.3372549 , 1.        ]]], dtype=float32)"
      ]
     },
     "execution_count": 166,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "car[:1]"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<img src=\"images/dog-photo.png\" />"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 167,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "<class 'numpy.ndarray'>\n"
     ]
    }
   ],
   "source": [
    "dog = imread(\"images/dog-photo.png\")\n",
    "print(type(dog))"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 168,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "array([[[0.70980394, 0.80784315, 0.88235295, 1.        ],\n",
       "        [0.72156864, 0.8117647 , 0.8862745 , 1.        ],\n",
       "        [0.7411765 , 0.8156863 , 0.8862745 , 1.        ],\n",
       "        ...,\n",
       "        [0.49803922, 0.6862745 , 0.8392157 , 1.        ],\n",
       "        [0.49411765, 0.68235296, 0.8392157 , 1.        ],\n",
       "        [0.49411765, 0.68235296, 0.8352941 , 1.        ]],\n",
       "\n",
       "       [[0.69411767, 0.8039216 , 0.8862745 , 1.        ],\n",
       "        [0.7019608 , 0.8039216 , 0.88235295, 1.        ],\n",
       "        [0.7058824 , 0.80784315, 0.88235295, 1.        ],\n",
       "        ...,\n",
       "        [0.5019608 , 0.6862745 , 0.84705883, 1.        ],\n",
       "        [0.49411765, 0.68235296, 0.84313726, 1.        ],\n",
       "        [0.49411765, 0.68235296, 0.8392157 , 1.        ]],\n",
       "\n",
       "       [[0.6901961 , 0.8       , 0.88235295, 1.        ],\n",
       "        [0.69803923, 0.8039216 , 0.88235295, 1.        ],\n",
       "        [0.7058824 , 0.80784315, 0.88235295, 1.        ],\n",
       "        ...,\n",
       "        [0.5019608 , 0.6862745 , 0.84705883, 1.        ],\n",
       "        [0.49803922, 0.6862745 , 0.84313726, 1.        ],\n",
       "        [0.49803922, 0.6862745 , 0.84313726, 1.        ]],\n",
       "\n",
       "       ...,\n",
       "\n",
       "       [[0.9098039 , 0.81960785, 0.654902  , 1.        ],\n",
       "        [0.8352941 , 0.7490196 , 0.6509804 , 1.        ],\n",
       "        [0.72156864, 0.6313726 , 0.5372549 , 1.        ],\n",
       "        ...,\n",
       "        [0.01568628, 0.07058824, 0.02352941, 1.        ],\n",
       "        [0.03921569, 0.09411765, 0.03529412, 1.        ],\n",
       "        [0.03921569, 0.09019608, 0.05490196, 1.        ]],\n",
       "\n",
       "       [[0.9137255 , 0.83137256, 0.6784314 , 1.        ],\n",
       "        [0.8117647 , 0.7294118 , 0.627451  , 1.        ],\n",
       "        [0.65882355, 0.5686275 , 0.47843137, 1.        ],\n",
       "        ...,\n",
       "        [0.00392157, 0.05490196, 0.03529412, 1.        ],\n",
       "        [0.03137255, 0.09019608, 0.05490196, 1.        ],\n",
       "        [0.04705882, 0.10588235, 0.06666667, 1.        ]],\n",
       "\n",
       "       [[0.9137255 , 0.83137256, 0.68235296, 1.        ],\n",
       "        [0.76862746, 0.68235296, 0.5882353 , 1.        ],\n",
       "        [0.59607846, 0.5058824 , 0.44313726, 1.        ],\n",
       "        ...,\n",
       "        [0.03921569, 0.10196079, 0.07058824, 1.        ],\n",
       "        [0.02745098, 0.08235294, 0.05882353, 1.        ],\n",
       "        [0.05098039, 0.11372549, 0.07058824, 1.        ]]], dtype=float32)"
      ]
     },
     "execution_count": 168,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "dog"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.8.3"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 4
}
