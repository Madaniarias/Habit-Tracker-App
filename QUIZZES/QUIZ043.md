# QUIZ043

## INSTRCUTIONS
![Screen Shot 2023-02-28 at 9 46 31](https://user-images.githubusercontent.com/111761417/221723158-333eb4fd-41ee-46c9-ad7a-2efd4cdc0643.png)

## SQL COMMAND
```.py
attach database "movies" as db;
CREATE TABLE if not exists movies(
    id INTEGER PRIMARY KEY,
    name text,
    producer text,
    director text,
    category text,
    budget INTEGER,
    year INTEGER);

INSERT INTO movies(name,producer,director,category,budget,year) VALUES ('17 Again','Adam Shankman and Jennifer Gibgot','Bur Steers','Comedy','40000000','2009');
INSERT INTO movies(name, producer, director, category, budget, year) VALUES ('Encanto','Yvett Merino and Clark Spencer','Jared Bush and Byron Howard','Computer-animated musical fantasy comedy ','150000000','2021');
```

## TEST

![Screen Shot 2023-03-25 at 15 55 54](https://user-images.githubusercontent.com/111761417/227702096-fc38957d-3955-4669-b4f5-f3147b405b49.png)

![Screen Shot 2023-03-25 at 15 56 24](https://user-images.githubusercontent.com/111761417/227702100-1190f6c0-69d1-4c17-8b82-a8d3bef854ac.png)
