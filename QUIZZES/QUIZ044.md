# QUIZ044

## INSTRCUTIONS

![Screen Shot 2023-02-28 at 9 48 34](https://user-images.githubusercontent.com/111761417/221723432-29bf3234-495d-4648-a6c7-30594ae68d9f.png)

## ANSWERS

1. How many tables are there in the database?

A/. There are 3 tables in the database

2. How many Male inhabitants are Friendly?

A/. There are 4 inhabitants that are friendly

3. What is the average gold by village?

A/. The average gold per village is:

VILLAGEID 1 = 129.1666666
VILLAGEID 2 = 112.5
VILLAGEID 3 = 137.5
VILLAGEID 4 = 118.75

4. How many items are there that start with the letter “A”

A/. There are 3 items that atrta with the letter A

5. How many different jobs are there? 

A/. There are 15 different jobs.

6. What are the items owned by the herbalists?

A/. There item owned by herbalist is the dagger.


## SQL COMMAND + TEST

1. How many tables are there in the database?

```.py
SELECT count(*) from sqlite_master WHERE type is 'table';
```
![Screen Shot 2023-03-25 at 16 09 20](https://user-images.githubusercontent.com/111761417/227702687-83746ff9-7d2e-4a2f-bd90-c1dd1592474e.png)

2. How many Male inhabitants are Friendly?

```.py
SELECT count(*) from INHABITANT WHERE gender is 'Male' and state is 'Friendly';
```
![Screen Shot 2023-03-25 at 16 10 11](https://user-images.githubusercontent.com/111761417/227702719-cf36704a-f4da-4b90-868d-6e841db49852.png)

3. What is the average gold by village?

```.py
SELECT avg(gold), villageid from INHABITANT GROUP BY villageid;
```
![Screen Shot 2023-03-25 at 16 11 08](https://user-images.githubusercontent.com/111761417/227702747-c8567a46-c178-44c7-b029-f67058489155.png)

4. How many items are there that start with the letter “A”

```.py
SELECT count(*) from ITEM where item like 'A%';
```
![Screen Shot 2023-03-25 at 16 11 44](https://user-images.githubusercontent.com/111761417/227702772-7bf9f4c7-1fe2-4428-8433-887c52309b6b.png)

5. How many different jobs are there? 

```.py
SELECT count(distinct job) from  INHABITANT;
```
![Screen Shot 2023-03-25 at 16 12 22](https://user-images.githubusercontent.com/111761417/227702798-fc8dac77-1d6c-4dce-99fa-c24dc6ab1f95.png)

6. What are the items owned by the herbalists?

```.py
SELECT personid from INHABITANT where job is 'Herbalist';
SELECT * from ITEM where owner = 4 or owner = 18;
```
![Screen Shot 2023-03-25 at 16 13 44](https://user-images.githubusercontent.com/111761417/227702872-6f15d3b4-ce79-4673-9cf3-a35803338eca.png)


