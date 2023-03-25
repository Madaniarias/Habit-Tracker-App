# QUIZ046

## INSTRCUTIONS
![Screen Shot 2023-02-28 at 9 51 41](https://user-images.githubusercontent.com/111761417/221725407-b472efda-7537-47d9-a295-30210a4443e7.png)

## CODE
```.py
#quiz46

import sqlite3

haiku = """Code flows like a stream
 Algarithms guide its way
 In silence, it solves"""
class database_handler():
    def __init__(self, namedb: str):
        self.connection = sqlite3.connect(namedb)
        self.cursor = self.connection.cursor()

    def create_table(self):
        query = f"""CREATE TABLE if not exists words(
            id INTEGER PRIMARY KEY not NULL,
            word text not NULL,
            length int not NULL
            )"""
        self.run_query(query)

    def run_query(self, query: str):
        self.cursor.execute(query)
        self.connection.commit()

    def close(self):
        self.connection.close()

db = database_handler(namedb = "quiz046.db")
db.create_table()

for word in haiku.split():
    query = f"INSERT into words (word,length) VALUES ('{word}',{len(word)})"
    db.run_query(query)

query = f"SELECT avg(length) from words as 'average_len'"
db.run_query(query)
print(db.cursor.fetchone())

db.close()
```

## TEST

![Screen Shot 2023-03-25 at 16 39 38](https://user-images.githubusercontent.com/111761417/227704195-620276b8-9eff-48f9-931f-da714c416ee1.png)

