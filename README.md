# Spring Hibernate App

This repository contains a simple Spring MVC web application integrated with Hibernate for data persistence.

## Project Structure

- **config**: Contains Spring configuration classes.
- **controllers**: Contains Spring MVC controller classes.
- **dao**: Contains Data Access Object (DAO) classes for interacting with the database.
- **models**: Contains entity classes representing database tables.

## How Spring and Hibernate Work Together

Spring and Hibernate work together seamlessly to provide a robust framework for building web applications with database connectivity and ORM capabilities.

### Spring Configuration

In the Spring configuration, beans are defined and managed by the Spring container. Spring manages the application's components and their dependencies, enabling loose coupling and easier integration. In this project, Spring is configured to handle MVC architecture and integrates Hibernate for database interaction.

### Hibernate Configuration

Hibernate, on the other hand, is responsible for Object-Relational Mapping (ORM), which bridges the gap between Java objects and relational database tables. It provides a set of APIs for performing CRUD operations on database entities. Hibernate configuration includes defining the data source, session factory, transaction manager, and entity mappings.

### Spring MVC Controllers

Spring MVC controllers handle incoming HTTP requests and delegate the business logic to other components, such as DAOs. In this project, controllers are responsible for processing requests related to people, such as displaying a list of people, showing details of a person, adding a new person, editing existing people, and deleting people.

### Data Access Objects (DAOs)

DAOs encapsulate the logic for interacting with the database. They use Hibernate's session factory to execute queries and transactions, abstracting away the underlying database details. DAOs provide methods for performing CRUD operations on database entities, enabling modular and reusable database access logic.

### Entity Classes

Entity classes represent database tables and are annotated with JPA annotations. These annotations define the mapping between Java objects and database tables, allowing Hibernate to manage the persistence of these entities. Entity classes encapsulate data and behavior related to specific database tables, providing a convenient way to interact with database entities in the application.

## Project Logic

1. **User Interaction**: Users interact with the application through a web interface, accessing various functionalities provided by the Spring MVC controllers.
2. **Controller Handling**: Spring MVC controllers process incoming requests, invoking appropriate methods to perform the requested actions, such as fetching data from the database or updating database records.
3. **Data Persistence**: Hibernate manages the persistence of data, handling the mapping between Java objects and database tables. It ensures that changes made to Java objects are reflected in the database and vice versa.
4. **Database Interaction**: DAOs provide a layer of abstraction over database access, encapsulating the logic for CRUD operations. They interact with the Hibernate session factory to execute queries and transactions, ensuring efficient and secure database access.
5. **Response Rendering**: The application generates responses dynamically, rendering views using Thymeleaf templates configured in the Spring configuration. These views present data retrieved from the database to the user, facilitating a rich and interactive user experience.

## Running the Application

To run the application, you need to configure a database connection in the `hibernate.properties` file and deploy it to a Servlet container such as Tomcat.
