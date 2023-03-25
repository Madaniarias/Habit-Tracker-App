# QUIZ048

## INSTRCUTIONS
![Screen Shot 2023-02-28 at 10 07 50](https://user-images.githubusercontent.com/111761417/221725971-445790bd-a761-47af-84b5-6248899c4cf5.png)

## CODE
```.py
import sqlite3
from HABIT_TRACKER.secure_password import check_password


class database_worker:
    def __init__(self, name):
        self.connection = sqlite3.connect(name)
        self.cursor = self.connection.cursor()

    def search(self, query):
        result = self.cursor.execute(query).fetchall()
        return result

    def run_save(self, query):
        self.cursor.execute(query)
        self.connection.commit()

    def close(self):
        self.connection.close()


x = database_worker("bitcoin_exchange.db")
query = "SELECT * from ledger"
result = x.search(query)
print(result)

for item in result:
    id = item[0]
    sender_id = item[1]
    receiver_id = item[2]
    amount = item[3]

    string = f"id {id},sender_id {sender_id},receiver_id {receiver_id},amount {amount}"

    check_hash = check_password(string, item[4])

    if check_hash == True:
        msg = f"Tx(id={id})Signature matches"
        print(msg)
    else:
        msg = f"Tx(id={id})Error signature"
        print(msg)

x.close()
```
## TEST

![Screen Shot 2023-03-25 at 16 54 09](https://user-images.githubusercontent.com/111761417/227704966-b8a3cbd5-84d0-407a-87fb-e983e66d6746.png)

