# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 77 records.

select products.productName, categories.categoryName from products 
join categories on categories.categoryId = products.categoryId;

### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.

select orders.orderId, shippers.shipperName from orders 
join shippers on shippers.shipperId = orders.shipperId
WHERE orders.orderDate < '1997-01-09'

### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.

select products.productName, orderDetails.quantity from orderDetails
join products on products.productId = orderDetails.productId
join orders on orders.orderId = orderDetails.orderId where orders.orderId = 10251 order By productName

### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.

select orders.orderId, customers.customerName, employees.lastName from orders 
join customers on customers.customerId = orders.customerId
join employees on employees.employeeId = orders.employeeId

### (Stretch)  Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

### (Stretch) Display OrderID and a  column called ItemCount that shows the total number of products placed on the order. Shows 196 records. 