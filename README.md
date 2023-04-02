<h1 align="center">
  <br>
<a  href="https://spring.io/"  target="_blank"  rel="noreferrer"> <img  src="https://www.vectorlogo.zone/logos/springio/springio-icon.svg"  alt="spring"  width="180"  height="180"/> </a>
  <br>
  <br>
  Spring Final Project
  <br>
  <br>
</h1>

<p align="center">
  <a href="#project-description">Project Description</a> |
  <a href="#tech-stack-and-libraries">Tech Stack and Libraries</a> |
  <a href="#how-it-works">How it Works</a> |
  <a href="#code-examples">Code Examples</a> |
  <a href="#acknowledgements">Acknowledgements</a>
</p>



<div id="project-description"></div>

## 🚀 Project Description
Taco Cloud is a multi-module Maven project that serves as a comprehensive example of building a REST API using Spring. The project includes modules such as the REST API, persistence, messaging, security, email integration, and a UI built with Angular. The project utilizes Spring technologies such as Spring WebFlux, Spring Data, Spring Integration, and Spring Security to provide a complete end-to-end solution.

The Taco Cloud project also includes modules for messaging using JMS, RabbitMQ, and Kafka, allowing the application to communicate with external services. The email integration module demonstrates how to handle orders through email using Spring Integration. Additionally, the project includes a client module that demonstrates how to consume the REST API exposed by the Taco Cloud application using RestTemplate and Traverson.

The project provides a comprehensive example of using Spring to build a complete web application, from the REST API to the UI, while showcasing best practices in modern web development.


<div id="tech-stack-and-libraries"></div>

## 🛠️ Tech Stack and Libraries
- Backend Technologies : 
  - Java 11
  - Spring Framework 5.3 (including Spring Boot, Spring Data, Spring Security, Spring Integration, Spring WebFlux)
  - MongoDB 4.4
  - RabbitMQ 3.8
  - Apache Kafka 2.7
  - Apache ActiveMQ 5.16
- Frontend Technologies:
  - TypeScript
  - Angular 11
  - Bootstrap 4
- Additional Libraries :
  - Lombok 1.18 - Used for reducing boilerplate code in the Java classes
  - MapStruct 1.4 - Used for generating type-safe mappers between Java objects
  - Jackson 2.12 - Used for JSON serialization and deserialization
  - Apache Maven 3.8 - Used for project management and build automation
  - JUnit 5 - Used for unit testing
  - Mockito 3 - Used for mocking and testing
  - RestTemplate - Used for making HTTP requests to external services

<div id="how-it-works"></div>

## ⚙️ How it Works

The Taco Cloud project is a multi-module Maven project that includes a REST API, several messaging modules, a UI, and other supporting modules.

The API is built using Spring WebFlux and exposes endpoints for managing tacos and placing orders. The API data is persisted using MongoDB, with support for reactive programming provided by Spring Data. The messaging modules use JMS, Kafka, and RabbitMQ to send messages related to order processing and kitchen operations. The UI is built using Angular and communicates with the API using HTTP requests.

When an order is placed through the UI or the API, a message is sent to the appropriate messaging module, which then sends messages to the kitchen application and other interested parties. The kitchen application receives the order message, prepares the tacos, and sends a message back to the messaging module indicating that the order is ready. The messaging module then sends a notification to the customer via email, and updates the order status in the database.

Overall, the Taco Cloud project demonstrates how to build a modern, cloud-native web application using Spring, reactive programming, and messaging.

<div id="code-examples"></div>

## 💡 Features
**1. User authentication and authorization :** Users can create an account, log in, and log out. Different levels of access can be assigned to users, such as administrators, managers, and regular users.

**2. Create and customize tacos :** Users can create and customize tacos with a variety of ingredients and toppings. They can save their favorite combinations and share them with others.

**3. Place and track orders :** Users can place orders for tacos and track their status from preparation to delivery. They can view the estimated delivery time and receive notifications when their order is ready.

**4. Integration with third-party services :** The application can integrate with third-party services such as email providers, payment gateways, and social media platforms.

**5. Messaging and notifications :** The application can send messages and notifications to users via email, SMS, or push notifications. For example, users can receive order confirmations, delivery updates, and promotional offers.

**6. Analytics and reporting :** The application can collect and analyze data on user behavior, such as order history, preferences, and feedback. 


## 🏗️ Project Structure

 - `tacocloud-api` : The REST API. Modified to demonstrate Spring WebFlux.
 - `tacocloud-data-mongodb` : Mongo persistence module. Modified to demonstrate Spring Data's support for reactive programming.
 - `tacocloud-domain-mongodb` : The domain types
 - `tacocloud-email` : The email module that demonstrates using Spring Integration to handle orders by email.
 - `tacocloud-kitchen` : An application to be run in the Taco Cloud kitchen that will receive orders for kitchen staff to prepare.
 - `tacocloud-messaging-jms` : The Taco Cloud messaging module that sends messages using JMS.
 - `tacocloud-messaging-kafka` : The Taco Cloud messaging module that sends messages using Kafka.
 - `tacocloud-messaging-rabbitmq` : The Taco Cloud messaging module that sends messages using RabbitMQ.
 - `tacocloud-restclient` : Client code that consumes the API exposed from `tacocloud-api`.
 - `tacocloud-security` : The security module (TODO: Not fully functional yet.)
 - `tacocloud-ui` : A Typescript Angular UI
 - `tacocloud-web` : The web module (largely leftovers from previous chapters. TODO: Clean up and remove.)
 - `tacos` : The main module that pulls the other modules together and provides the Spring Boot main class.

<div id="acknowledgements"></div>

## 📚 Acknowledgements 
This project was created with the help of the book **"Spring in Action"** by **Craig Walls** and **Ryan Breidenbach**. Many of the concepts and techniques used in this project were learned from this valuable resource.

