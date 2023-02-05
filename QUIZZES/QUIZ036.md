# QUIZ036

## INSTRUCTIONS

HL: ① Create test cases for the classes below ② UML diagram. ③ Add another class Classroom which can store in a list student　objects, a method to add, remove students and method to calculate the average score.
![Screen Shot 2023-02-05 at 21 39 28](https://user-images.githubusercontent.com/111761417/216819173-31700063-d71c-42c8-9a3d-e30f0afc8b26.png)

## CODE

```.PY
class CompoundInterest:
    def __init__(self, principal: int, rate: int, no_years: int):
        self.principal = principal
        self.rate = rate
        self.no_years = no_years

    def calculate(self):
        equation = "{:.2f}".format(self.principal * (1 + self.rate) ** self.no_years)
        return equation


class AccountingProgram:

    def __init__(self):
        self.compound = CompoundInterest(0, 0, 0)

    def set_principal(self, principal):
        self.compound.principal = principal
        if principal <= 0:
            raise ValueError("Input need to be bigger than 0")
        return f"Principal set to {self.compound.principal}"

    def set_rate(self, rate):
        self.compound.rate = rate
        if rate <= 0:
            raise ValueError("Input need to be bigger than 0")
        return f"Principal set to {self.compound.rate}"

    def set_no_years(self, no_years):
        self.compound.no_years = no_years
        if no_years <= 0:
            raise ValueError("Input need to be bigger than 0")
        return f"Year set to {self.compound.no_years}"

    def calculate_interest(self):
        return self.compound.calculate()


compound_interest_calculator = CompoundInterest(principal=100, rate=0.1, no_years=10)
print(compound_interest_calculator.calculate())
```

## TEST
![Screen Shot 2023-02-06 at 1 00 11](https://user-images.githubusercontent.com/111761417/216830334-e94dadc6-a1bb-42d1-aa57-f3921f22d09b.png)


