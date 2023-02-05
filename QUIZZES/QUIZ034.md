# QUIZ034

## INSTRUCTIONS

Create a new Python function called to_roman(num) that takes a single integer as input. It returns a string representing the Roman numeral equivalent of the input number. 

Conditions: The function should only work for integers below 100, if the input is greater than 100, raise a ValueError with a message indicating that the input must be less than or equal to 100.

```.py
Example:
to_roman(37)  -> 'XXXVII'
to_roman(44)  -> 'XLIV'
to_roman(100) -> 'C'
to_roman(101) -> ValueError("Input number must be less than or equal to 100")
```

## CODE

```.py
#Create class quiz034
class quiz034:
    
    #initialize 
    def __init__(self, num:int):
        self.num = num
    
    #create method to_roman that takes a single integer as input. It returns a string representing the Roman numeral equivalent of the input number. 
    def to_roman(self)->str:
        num_rom = ""
        
        #Exception for when anything other than an integer is inputted
        if not isinstance(self.num,int):
            raise TypeError("Only integers are accepted")
            
        #Exception for when the number is not between 1 and 100
        if self.num > 100 or self.num <= 0:
            raise ValueError("The input must be between 1 and 100.")
        
        #Getting the roman numbers
        while self.num >0:
            for dig,i in [(100,'C'),(90,'XC'),(50,'L'),(40,'XL'),(10,'X'),(9,'IX'),(5,'V'),(4,'IV'),(1,'I')]:
                if self.num >= dig:
                    num_rom += i
                    self.num = self.num - dig
                    break

        return num_rom
```

## TEST FILE

```.py
from QUIZ034 import quiz034
import pytest


def test_to_roman():
    assert quiz034(num=1).to_roman() == 'I'
    assert quiz034(num=4).to_roman() == 'IV'
    assert quiz034(num=9).to_roman() == 'IX'
    assert quiz034(num=37).to_roman() == 'XXXVII'
    assert quiz034(num=44).to_roman() == 'XLIV'
    assert quiz034(num=50).to_roman() == 'L'
    assert quiz034(num=99).to_roman() == 'XCIX'
    assert quiz034(num=100).to_roman() == 'C'
    assert quiz034(num=77).to_roman() == 'LXXVII'
    assert quiz034(num=93).to_roman() == 'XCIII'


def test_to_roman_exceptions():
    # check that the program raises a ValueError
    with pytest.raises(ValueError):
        quiz034(num=101).to_roman()
```

## TEST EVIDENCE

![Screen Shot 2023-02-05 at 21 02 29](https://user-images.githubusercontent.com/111761417/216817541-895a1e54-3c63-4e86-8b37-8ea7b02053c6.png)


