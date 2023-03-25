# QUIZ045

## INSTRCUTIONS
![Screen Shot 2023-02-28 at 9 48 47](https://user-images.githubusercontent.com/111761417/221723523-188e08a3-6ed7-4698-9819-fb5a965206be.png)

## UML DIAGRAM
![Untitled Notebook (39)-1](https://user-images.githubusercontent.com/111761417/227703470-39873f41-3100-4372-b8c3-fdcde86d12f6.jpg)

## SQL QUERIES TO FIND RESPONSIBLE FOR FRAUDULENT TRANSACTION

```.py
SELECT account_id, sum(amount) as total_deposit FROM transactions where transaction_type = 'deposit' GROUP BY account_id; total deposit
SELECT account_id, sum(amount) as total_withdraw FROM transactions where transaction_type = 'withdraw' GROUP BY account_id; total withdraw
# group in legal or fraud transaction
SELECT CASE WHEN total_deposit - total_withdraw != balance THEN 'fraud' ELSE 'legal'
END AS 'Check', total_deposit, total_withdraw, balance, account_id
FROM (SELECT sum(amount) as total_deposit, account_id as 'account_deposit' FROM transactions where transaction_type = 'deposit' GROUP BY account_id ),
     (SELECT sum(amount) as total_withdraw, account_id as 'account_withdraw' FROM transactions where transaction_type = 'withdraw' GROUP BY account_id),
     accounts WHERE account_deposit = account_withdraw and account_deposit = accounts.account_id;
```
![Screen Shot 2023-03-25 at 16 31 30](https://user-images.githubusercontent.com/111761417/227703810-a1c01ebe-2de7-44a7-b03d-e740452de58e.png)

## NAME OF THE CUSTOMER AND THE PROBLEM THAT RESULTED IN THE BANKRUPTCY OF THE BANK

For the following costumer accounts the withdraw and deposit money does not match.

![Screen Shot 2023-03-25 at 16 34 06](https://user-images.githubusercontent.com/111761417/227703981-df279cd6-1572-4a2a-a87a-76b1e849acbb.png)
