# LibroSync

## Project Overview
LibroSync is a Spring Boot-based bookstore management system that enables users to browse, purchase, and manage books efficiently. It integrates authentication, order processing, and shopping cart functionalities while ensuring secure transactions and seamless user experience.

## Tech Stack
- **Java** - Core programming language
- **Spring Boot** - Backend framework
- **Spring Security** - Authentication and authorization
- **Hibernate** - ORM for database operations
- **H2 Database** - In-memory relational database
- **REST APIs** - Communication between services
- **Docker** - Containerization

## Project Structure
```
LibroSync/
|-- src/main/java/com/librosync/
|   |-- config/
|   |-- controller/
|       |-- BookController.java
|       |-- CartController.java
|       |-- CheckoutController.java
|       |-- HomeController.java
|       |-- LoginController.java
|       |-- OrderController.java
|   |-- model/
|       |-- Book.java
|       |-- Customer.java
|       |-- CustomerBooks.java
|       |-- Order.java
|   |-- repository/
|       |-- BillingRepository.java
|       |-- BookRepository.java
|       |-- OrderRepository.java
|   |-- security/
|       |-- SecurityConfig.java
|       |-- SecurityWebApplicationInitializer.java
|   |-- service/
|       |-- BillingService.java
|       |-- BookService.java
|       |-- EmailService.java
|       |-- ShoppingCartService.java
|-- src/main/resources/
|-- src/test/java/
|-- Dockerfile
|-- mvnw, mvnw.cmd
|-- pom.xml
```

## Key Features
### Controllers (API Endpoints)
- **BookController** - Manages book-related operations such as adding, updating, and retrieving books.
- **CartController** - Handles shopping cart functionalities like adding/removing books.
- **CheckoutController** - Processes orders and payments.
- **HomeController** - Manages the landing page and general navigation.
- **LoginController** - Manages authentication and user login.
- **OrderController** - Handles order placements and retrievals.

### Models
- **Book** - Represents book details such as title, author, and price.
- **Customer** - Stores customer-related information.
- **CustomerBooks** - Tracks books associated with a customer.
- **Order** - Represents order details and status.

### Repositories
- **BillingRepository** - Handles billing data operations.
- **BookRepository** - Manages book-related database transactions.
- **OrderRepository** - Stores order-related data.

### Services
- **BillingService** - Handles invoice generation and payments.
- **BookService** - Implements business logic for books.
- **EmailService** - Sends order confirmations and notifications.
- **ShoppingCartService** - Manages cart operations.

## Installation & Setup
### Prerequisites
- Java 8 or later
- Maven
- Docker (Optional for containerization)

### Steps to Run
1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/LibroSync.git
   ```
2. Navigate to the project directory:
   ```sh
   cd LibroSync
   ```
3. Configure the database in `application.properties`:
   ```properties
   spring.h2.console.enabled=true
   spring.datasource.url=jdbc:h2:mem:bookstore
   spring.datasource.driver-class-name=org.h2.Driver
   spring.datasource.username=your-username
   spring.datasource.password=your-password
   spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
   ```
4. Build and run the application:
   ```sh
   mvn spring-boot:run
   ```
5. (Optional) Run with Docker:
   ```sh
   docker build -t librosync .
   docker run -p 8080:8080 librosync
   ```

## Contributing
Feel free to submit issues or pull requests to improve the project.

## License
This project is licensed under the MIT License.

