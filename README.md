## Online-Enterprise-Management-System

# Proposed System Design:

	● We created a website that allows users to shop for clip-art stickers. The user can be a customer or admin. The website has a homepage, login, registration, products, and orders page.
 
	● Customers can change their profile details, view products and make orders. They can view their orders as well.
 
	● Admins can change user roles, view/modify/add/delete products, and view orders. They can update shipping dates and order status for the orders.
 
	● The shop calls a storage procedure to reduce the available products based on the order quantity.


# Configuration:
To generate a webpage as the “front end” or interface of our enterprise system, we used JSP/JAVA for server-side coding, JS for client-side validation, and CSS for the stylesheet.

	● We used springboot’s (2.2.4) embedded tomcat server application server.
 
	● We used springboot’s sts (3.9.12) for the workbench.
 
	● We used maven 3.9.1 for builds/packaging.
 
	● We used Postgres 15 (42.2.8) for the DBMS.
 
	● Java: JDK 1.8/11 virtual machine. JDBCtemplate was used to connect to the database and send queries


![image](https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/8339787b-1d1b-45bf-aa72-7219ba2885d6)

# Interface (Web-based):
The following screenshots demonstrate functionality of the proposed system design. There is a working interface in which the application successfully links the front-end and back-end.

	● Users are created, and are assigned a username and password.
 
	● Users have different privileges (non-user/user/admin). Non-users can only login or register. Users can view the shop and orders page. They can create orders and only view their own. Admins can update/delete products and view all user orders. However they can only modify the order status and shipping date.
 
	● There are atleast 3 different web pages for the interface


![image](https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/3903bd8b-8e3d-4955-9507-c3a149f1593b)


# Home page
We also have tabs with Login and Register included at the top to allow the user to either login with pre existing credentials or create new credentials to shop online.


![image](https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/e9283929-0f19-4696-b1aa-8cfa5a63143e)


# User registration Page
we can input a first name, last name, user name, password, address, and email id.
There is input validation for each of these required fields.
If a field is left empty, the website lets you know which field must be filled out.
We have also included input validation for the password data entry, where it needs to follow the guidelines of having one upper case, one lower case, and one number.
The e-mail must also be in the correct format.


![image](https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/81a0f4fd-f000-420f-9429-1de25b33e6d0)


# User login page


![image](https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/cfb076f0-1606-45e3-bcc6-6d6be3795017)


# Register succeeded!
We can see our credentials that we registered into the system, not only on the registration page.


![image](https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/8c123408-5a0d-4eb2-aea7-45f237f7481e)

# Welcome
After logging in, we are met with a lovely screen that shows a “Hello” name tag with the first and last name inputted by the user when registering– and the role of the user shown at the bottom. Every user can either have the role of an admin, or a user.
Users have the basic ability to change their profile details in the profile tab, view products and make orders in the shop tab and can also view their own orders, in the orders tab at the top.


![image](https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/6fbff6eb-80de-4e84-813c-058b299a0eee)

# Profile
Here we can see our profile details that we entered when we first registered, we also have the ability to edit here (with the same input validations required during registering). After hitting save the user can see that the user profile has saved successfully with the message at the top. On the welcome page, the name will be updated.


![image](https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/d89c459d-86da-46d1-89ce-40468b62bb51)

# Shop
Shop tab. Here we can see the product list. Customers can only see the products with an available quantity that is greater than 0.
This is where we can buy any quantity of stickers and view the price. However, an important thing to mark here is that you can only order less than or equal to the quantity listed next to each product. This is another kind of validation that we added.
You also cannot order a negative amount (or you will receive an error).


![image](https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/8bc54e11-bdd8-4234-8e2b-c74445b22de3)

# Order Confirmation
order confirmation: we can see the order details of what we just placed. The important thing to note here is that we now have an order ID for the order, a user associated with the order, and an order status of created along with the date and time stamp of when the order was placed.


![image](https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/5e4032b6-8b71-4a57-9b25-d537c5f350dc)


# Admin view:
Admins can change user roles/details (except for the username/passwords), view/modify/add/delete products, and view orders. They can update shipping dates and order status for the orders (as canceled, created, shipped, delivered).
Instead of the profile page, the admin sees a User Administration page where I can see all of the profile details of all of the users of the website, except for their passwords of course.
I can update profile details except for the username/password.


![image](https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/9956ef26-3b6a-4c53-91fd-cb7e4677bccf)


# Admin view: Store inventory
Here we add, delete, and modify products.
To add a product there is input validation where the quantity and price fields must be entered. The quantity must be >0 and the price must be a number >0
We can restock the stickers as well.


![image](https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/93254ce7-7630-43a0-8e42-a1189b708b36)


# Admin order history:
Here, the admin can see the order history of all users! We cannot delete orders however, as it is important to keep a log of all of them. We can however change the order status from created to delivered, shipped, and cancelled.
Marking an order as delivered/shipped will update the timestamp. However, if we cancel an order, the stock updates in the inventory!











