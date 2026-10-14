PRACTITIONER

LAB Solved

This lab contains a SQL injection vulnerability in the product category filter. The results from the query are returned in the application's response, so you can use a UNION attack to retrieve data from other tables. To construct such an attack, you first need to determine the number of columns returned by the query. You can do this using a technique you learned in a previous lab. The next step is to identify a column that is compatible with string data.

The lab will provide a random value that you need to make appear within the query results. To solve the lab, perform a SQL injection UNION attack that returns an additional row containing the value provided. This technique helps you determine which columns are compatible with string data.

First of all lets if we can get a 500

![](../../attachments/Pasted%20image%2020261014185901.png)

Amazing lets move one first of all since we already know the DB's so we are going to use that in our side in other case you might need to know who you are dealing with then move on 

`' UNION SELECT NULL FROM DUAL--`

we are on the right path: 


![](../../attachments/Pasted%20image%2020261014190249.png)

Lets move one and see :
