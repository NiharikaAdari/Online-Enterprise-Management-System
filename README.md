# Online-Enterprise-Management-System
Proposed System Design:

	● We created a website that allows users to shop for clip-art stickers. The user can be a customer or admin. The website has a homepage, login, registration, products, and orders page.
 
	● Customers can change their profile details, view products and make orders. They can view their orders as well.
 
	● Admins can change user roles, view/modify/add/delete products, and view orders. They can update shipping dates and order status for the orders.
 
	● The shop calls a storage procedure to reduce the available products based on the order quantity.


Configuration:
To generate a webpage as the “front end” or interface of our enterprise system, we used JSP/JAVA for server-side coding, JS for client-side validation, and CSS for the stylesheet.

	● We used springboot’s (2.2.4) embedded tomcat server application server.
 
	● We used springboot’s sts (3.9.12) for the workbench.
 
	● We used maven 3.9.1 for builds/packaging.
 
	● We used Postgres 15 (42.2.8) for the DBMS.
 
	● Java: JDK 1.8/11 virtual machine. JDBCtemplate was used to connect to the database and send queries


![image](https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/8339787b-1d1b-45bf-aa72-7219ba2885d6)

Interface (Web-based):
The following screenshots demonstrate functionality of the proposed system design. There is a working interface in which the application successfully links the front-end and back-end.

	● Users are created, and are assigned a username and password.
 
	● Users have different privileges (non-user/user/admin). Non-users can only login or register. Users can view the shop and orders page. They can create orders and only view their own. Admins can update/delete products and view all user orders. However they can only modify the order status and shipping date.
 
	● There are atleast 3 different web pages for the interface



Home: <img width="523" alt="image" src="https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/5d489268-3e16-460b-9980-f00980609be8">


Login: <img width="515" alt="image" src="https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/435e69c7-778b-4a70-9d58-46f998ff35e9">


Register: <img width="508" alt="image" src="https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/14100c80-86a3-40f9-88f9-8d19354e6a70">


1. <img width="319" alt="image" src="https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/aa1c0aa6-ceb0-4eba-a18f-dbb70ef1fe18">


2. <img width="312" alt="image" src="https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/50f6e415-ef87-49f4-a857-a5fb403993d0">


3. <img width="313" alt="image" src="https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/895412f8-62ad-45d1-97c8-872de1b4295c">


4. <img width="313" alt="image" src="https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/0bbe20d5-2322-4a05-b345-5b7e1e49ca5a">


5. <img width="312" alt="image" src="https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/8b5947ac-e95e-427c-9a61-30d129d40ce7">


6. <img width="313" alt="image" src="https://github.com/NiharikaAdari/Online-Enterprise-Management-System/assets/130190699/5d3c0673-64f1-4718-a17d-d12e3742c8ac">
















