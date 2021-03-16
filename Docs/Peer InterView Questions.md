# Interview Questions


## 1. What is C#
 
- C# is a strongly and statically typed object-oriented programming language 
 
## 2. What is an instance in object-oriented programming? 
 
- An instance is an object that is an instance of a class or type 
 
## 3. Explain the difference between class/static methods and instance methods 
 
- Static methods belong to the class itself 
-> ClassName.MethodName()
 
- Instance methods require an instance of a class in order to call the method-> instanceName.MethodName()
 
## 4. You have a table called DRIVERS and a table called ORDERS.  Orders are delivered by drivers. In this way, the orders belong to a driver through the column orders.driver_id.  Write a SQL expression that gets all the drivers that have delivered an order 
 
 ```sql
SELECT * FROM DRIVERS
INNER JOIN ORDERS 
ON ORDERS.DRIVER_ID = DRIVERS.ID;
```
 
 
## 5. What does REST stand for and what are 4 restful verbs?
 
- Representational State Transfer
- POST 
- GET 
- PUT 
- DELETE
 
 
## 6. Explain what an ORM is and what it does
 
- Object Relational Mapper:
- An ORM is used to access a relational database from an   object-oriented language 

