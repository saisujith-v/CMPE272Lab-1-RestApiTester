# Simple REST Service

This is a simple RESTful web service built using Spring Boot. It provides a basic greeting message that can be customized using a query parameter.

## Features

- Spring Boot 2.7.0
- REST API with `/greeting` endpoint
- JSON response with an ID and a greeting message
- Customizable message by passing a `name` parameter in the request
- Quick and easy project setup using Spring Initializr

## Tools and Technologies Used

- **Java 11** or above
- **Spring Boot 2.7.0**
- **Maven** for dependency management and build automation
- **Postman** (or any other REST client) for testing the API

## Getting Started

### Prerequisites

Before running this application, ensure you have the following installed on your system:

- Java 11 or higher
- Maven
- A code editor or IDE (e.g., IntelliJ IDEA, Eclipse)

### Project Setup

1. Clone the repository or download the source code:
    ```bash
    git clone https://github.com/your-username/simple-rest-service.git
    ```

2. Navigate into the project directory:
    ```bash
    cd simple-rest-service
    ```

3. Open the project in your preferred IDE (IntelliJ IDEA, Eclipse, etc.) as a **Maven project**.

4. Ensure the following dependencies are present in the `pom.xml` file:
    - Spring Web
    - Spring Boot Starter
    - Spring Boot Maven Plugin

5. Run the application:
    - You can run the application by executing the following Maven command in the terminal:
      ```bash
      mvn spring-boot:run
      ```
    - Alternatively, right-click on the `SimpleRestServiceApplication` class in your IDE and choose `Run`.

6. Once the application starts, it will run on the default port **8080**.

### Testing the REST API

1. **Default Greeting**:
    - Open Postman (or your preferred REST client).
    - Send a **GET** request to the following URL:
      ```
      http://localhost:8080/greeting
      ```
    - The response should be:
      ```json
      {
          "id": 1,
          "content": "Hello, World!"
      }
      ```

2. **Custom Greeting**:
    - You can customize the greeting by adding a `name` query parameter:
      ```
      http://localhost:8080/greeting?name=John
      ```
    - The response should be:
      ```json
      {
          "id": 2,
          "content": "Hello, John!"
      }
      ```

### Project Structure

- `src/main/java/com/example/simplerestservice`:
  - **model**: Contains the `Greeting` class.
  - **controller**: Contains the `GreetingController` class with the `/greeting` endpoint.
  - **SimpleRestServiceApplication**: The main entry point of the Spring Boot application.
