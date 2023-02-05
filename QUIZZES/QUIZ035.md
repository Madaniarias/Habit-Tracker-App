# QUIZ035

## INSTRUCTIONS

Create a Python class for a Bank Office that follows the UML diagram below and passes the test file test_quiz35.py
![Screen Shot 2023-02-05 at 21 10 09](https://user-images.githubusercontent.com/111761417/216817918-ce0060f0-4375-446c-a857-917d9a603727.png)

## CODE

```.PY
#QUIZ035.py

#importing random to generate random account number
import random
#importing pytest to test the program
import pytest

#create class Account
class Account:
    #initialize
    def __init__(self):
        self.holder_name = ""
        self.holder_email = ""
        self.balance = 0
        
        #use random to create random account number
        a = random.randint(100, 1000)
        b = random.randint(10000, 100000)
        c = random.randint(1, 10)
        self.number = [a, b, c]
    
    #create method set_holder_name
    def set_holder_name(self, name: str) -> str:
        self.holder_name = name
        
    #Exception: if input is not a string show error
        if not isinstance(self.holder_name, str):
            raise ValueError("Error. Input your name")
        return f"Holder's name set to {name}"
        
    #create method set_holder_email
    def set_holder_email(self, email: str) -> str:
        self.holder_email = email
        
        #Exceptions: if there is more than one @ in the input show error
        counter = 0
        for i in self.holder_email:
            if i is "@":
                counter += 1
            if counter > 1:
                raise ValueError()
        return f"Holder's email set to {email}"
        
    #create method deposit
    def deposit(self, amount: int) -> str:
        self.balance += amount
        return f"New balance: {self.balance} USD"
        
    #create method get_balance
    def get_balance(self) -> int:
        return self.balance
    
    #create method get_account_no
    def get_account_no(self) -> str:
        a, b, c = self.number
        return f"{a}-{b}-{c}"
```

## TEST FILE

```.PY
import pytest
from QUIZ035 import Account


def test_empty_account():
    bk = Account()
    assert bk.balance == 0
    assert bk.holder_name == ""
    assert bk.holder_email == ""
    assert isinstance(bk.number, list)
    number = bk.get_account_no().split("-")
    assert len(number) == 3 and len(number[0]) == 3 and len(number[1]) == 5 and len(number[2]) == 1


def test_create_account():
    bk = Account()
    assert bk.get_balance() == 0
    assert bk.set_holder_name(name="Bob") == "Holder's name set to Bob"
    assert bk.set_holder_email(email="bob@company.xyz") == "Holder's email set to bob@company.xyz"
    assert bk.deposit(amount=100) == "New balance: 100 USD"
    assert bk.get_balance() == 100


def test_value_errors():
    bk = Account()
    with pytest.raises(ValueError):
        bk.set_holder_email(email="bob@bob@bob")
        bk.set_holder_name(name=["Bob"])
        bk.set_holder_name(name=100)
```

## TEST

![Screen Shot 2023-02-05 at 21 36 41](https://user-images.githubusercontent.com/111761417/216819031-c9c95596-6e55-4ca2-8af8-273f88461b18.png)

