# Shopify-challenge

Question 1 (a) Shop id 42 has large orders of 2000 units and Shop id 78 per unit price is coming as 25725 thus inflating the average of the whole dataset. Better way to evaluate data is to find per unit price of the sneaker sold by 100 shops, remove any noise and outliers before finding the AOV from the rest of the dataset. 

(b) For the data set I would report the average selling price of sneaker to  help analyse the average profit and the number of units sold can help to decide production to meet the demand.

(c) Average sneaker selling price (excluding shop id 42 and 78) is $150.40



Question 2 (a) SELECT COUNT(ORDERID) FROM [Orders] WHERE SHIPPERID = 1 GROUP BY SHIPPERID;
Answer 54


(b) select [employees].lastname, [orders].employeeid, count ([orders].orderid) from [orders] join [employees] on [orders].employeeid = [employees].employeeid group by [orders].employeeid order by count ([orders].orderid) DESC;
Answer Lastname Peacock employee id 4 number of orders 40


(c)SELECT [products].productname, [customers].country, [orders].customerid, [orderdetails].productid, count([orderdetails].productid) FROM [orders], [orderdetails], [customers], [products] where [orders].orderid = [orderdetails].orderid AND [orders].customerid = [customers].customerid AND [orderdetails].productid = [products].productid AND country = 'Germany' group by [products].productid order by count([orderdetails].productid) DESC;
Answer Product name Gorgonzola Telino
