# QUIZ037

## INSTRUCTIONS



## CODE

```.PY
#Create class CompoundInterest
class CompoundInterest:
    #initialize
    def __init__(self, principal: int, rate: int, no_years: int):
        self.principal = principal
        self.rate = rate
        self.no_years = no_years
    
    #create method for the compound interest equation
    def calculate(self):
    
        #set equation for compound interest and rounding the result.
        equation = "{:.2f}".format(self.principal * (1 + self.rate) ** self.no_years)
        return equation


#Create class AccountingProgram
class AccountingProgram:
    
    #initialize
    def __init__(self):
        self.compound = CompoundInterest(0, 0, 0)
        
    #Create Method to set the principal
    def set_principal(self, principal):
        self.compound.principal = principal
        
        #Exception: if the principal is equal or less than 0, show an error.
        if principal <= 0:
            raise ValueError("Input need to be bigger than 0")
        return f"Principal set to {self.compound.principal}"
    
    #Create a Method to set the rate
    def set_rate(self, rate):
        self.compound.rate = rate
        
        #Exception: if the rate is equal or less than 0, show an error.
        if rate <= 0:
            raise ValueError("Input need to be bigger than 0")
        return f"Principal set to {self.compound.rate}"
   
    #Create a Method to set the number of years
    def set_no_years(self, no_years):
        self.compound.no_years = no_years
        
        #Exception: if the number of years is equal or less than 0, show an error.
        if no_years <= 0:
            raise ValueError("Input need to be bigger than 0")
        return f"Year set to {self.compound.no_years}"

    #Create a Method that uses the equation created in the class Compound interest
    def calculate_interest(self):
        return self.compound.calculate()

#Create an object and run.
compound_interest_calculator = CompoundInterest(principal=100, rate=0.1, no_years=10)
print(compound_interest_calculator.calculate())
```

## TEST
![Screen Shot 2023-02-06 at 1 00 11](https://user-images.githubusercontent.com/111761417/216830334-e94dadc6-a1bb-42d1-aa57-f3921f22d09b.png)


