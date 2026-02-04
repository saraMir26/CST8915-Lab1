# CST8915 Lab 1: Algonquin Pet Store on Azure VM

**Student Name**: Sara Mirzaei
**Student ID**: 040467655
**Course**: CST8915 Full-stack Cloud-native Development  
**Semester**: Winter 2026  

---

## Demo Video

🎥 **YouTube Demo (Unlisted)**  
👉 [https://www.youtube.com/watch?v=YOUR_VIDEO_ID](https://youtu.be/921S69gyN-Y)

This video demonstrates the Algonquin Pet Store application running on an Azure Virtual Machine, including product browsing, order placement, and message queuing with RabbitMQ.

---

## Technical Explanations

### Order Service (Node.js)

The Order Service is responsible for handling customer orders submitted from the store front. When a user places an order, this service receives the request through a REST API, validates the order data, and publishes an order message to RabbitMQ. This design ensures that order processing is reliable and decoupled from other services in the system.

---

### Product Service (Rust)

The Product Service manages the product catalog, including product names, descriptions, prices, and inventory data. It exposes REST API endpoints that allow other services, such as the store front, to retrieve product information. This service ensures that product data is centralized and consistently available.

---

### Store Front (Vue.js)

The Store Front is the customer-facing web application where users browse products, add items to their cart, and place orders. It retrieves product data from the Product Service and submits orders to the Order Service using HTTP requests. This separation allows the UI to remain lightweight while relying on backend services for business logic. 
The application is built with Vue.js, 

---

## Challenges and Learnings (Optional)

During this lab, I learned how to deploy and configure multiple microservices on an Azure Virtual Machine. One challenge was correctly configuring Network Security Group rules to allow external access to the required ports. This lab helped reinforce concepts such as service dependency order, message-based communication, and cloud-based deployment.

---

## Acknowledgments

Course materials, official documentation for Azure, RabbitMQ, Node.js, Rust, and Vue.js were used as references during this lab.
