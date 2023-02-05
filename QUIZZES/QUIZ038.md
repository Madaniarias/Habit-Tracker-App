# QUIZ038

## INSTRUCTIONS

Create a program that creates the SalemanMap using your OOP code

## CODE

```.py
import math
import random
from matplotlib import pyplot as plt

random.seed(1234)


class coordinate:
    def __init__(self, x: int, y: int):
        self.x = x
        self.y = y

    def __repr__(self) -> str:
        return f"[Coordinate]x={self.x} y={self.y}"


class city:
    def __init__(self, name: str, location: coordinate):
        self.name = name
        self.location = location

    def __repr__(self) -> str:
        return f"[City class]A {self.name} located at {self.location}"

    def distance(self, city2):
        xa, xb = self.location.x, self.location.x
        ya, yb = city2.self.location.y, city2.self.location.y
        d = math.sqrt((xb - xa) ^ 2 + (yb - ya) ^ 2)
        return round(d, 2)


class country:
    def __init__(self, name: str):
        self.cities = []
        self.name = name

    def add_city(self, new_city: city):
        if isinstance(new_city, city):
            self.cities.append(new_city)
        else:
            raise ValueError("City must be a city object")

    def __repr__(self):
        return f"[Country object] Country "

Panama = country(name="Panama")
for n in ["Chiriqui", "Bocas", "Penonome", "Cocle", "Colon", "Herrera", "La Chorrera", "Los Santos", "Veraguas", "Darien"]:
    point = coordinate(x=random.randint(0, 9), y=random.randint(0, 9))
    new_city = city(name=n, location=point)
    Panama.add_city(new_city=new_city)
    plt.title("SalesmanMap")
    plt.scatter(point.x, point.y, color ="b", marker="*")
    plt.text(point.x, point.y, f"{new_city.name}")
plt.xlabel("Latitude(m)")
plt.ylabel("Longitude(m)")
plt.show()
```

## TEST

![image](https://user-images.githubusercontent.com/111761417/216832503-6a9ddbd8-ca98-41aa-97a6-5722fd1c29b1.png)

