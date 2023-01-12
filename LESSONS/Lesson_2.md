# EXCEPTIONS

TRying to divide a/b will be some exception. ex: cannot divibe by zero or thta an integer is entered.

```.py

#exceptions.py

def division(a:int, b:int)->float:
    if not isinstance(a,int):
        #not correct type of variable
        raise TypeError("Error. Input a must be integer")
    if not isinstance(b,int):
        #not correct type of variable
        raise TypeError("Error. Input a must be integer")
    if b==0:
        #not correct value (number)
        raise ValueError("Cannot divide by zero")


    return a/b

```

# ATOMATED TEST

```.py
#test_exceptions.py 

import pytest
from Exception import division

def test_valid():
    assert division(a=10,b=2) == 5
    assert division(a=5,b=2) == 2.5

def test_not_valid_inputs():
    with pytest.raises(ValueError):
        division(a=4,b=0)
    with pytest.raises(TypeError):
        division(a="helo",b=["world"])

```
