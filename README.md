# First Project: Java Spring Boot Demo

[![Ask DeepWiki](https://devin.ai/assets/askdeepwiki.png)](https://deepwiki.com/TuanBulut/first-project-java-spring)

This repository contains a simple demonstration project built with Java and the Spring Boot framework. It serves as a basic introduction to creating web applications with Spring, showcasing a simple REST endpoint and a dynamic web page using Thymeleaf.

## Features

*   **REST Endpoint:** A basic endpoint at `/` that returns a plain text greeting.
*   **Dynamic Web Page:** A `/greeting` endpoint that renders an HTML page using the Thymeleaf template engine.
*   **Query Parameter Handling:** The `/greeting` endpoint accepts an optional `name` query parameter to customize the greeting message.

## Technologies Used

*   **Java 17**
*   **Spring Boot 3.5.7**
    *   Spring Web
    *   Spring Boot Starter Thymeleaf
*   **Apache Maven**
*   **Lombok**

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

*   Java Development Kit (JDK) 17 or later.
*   Apache Maven is not required as the project includes the Maven Wrapper.

### Installation & Running

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/tuanbulut/first-project-java-spring.git
    ```

2.  **Navigate to the project directory:**
    ```sh
    cd first-project-java-spring
    ```

3.  **Run the application using the Maven Wrapper:**

    *   On macOS/Linux:
        ```sh
        ./mvnw spring-boot:run
        ```
    *   On Windows:
        ```sh
        mvnw.cmd spring-boot:run
        ```

The application will start and be available at `http://localhost:8080`.

## Usage

Once the application is running, you can access the following endpoints in your web browser or using a tool like `curl`:

*   **Root Endpoint:**
    *   URL: `http://localhost:8080/`
    *   Method: `GET`
    *   Response: A plain text string `Hello Vistula, in my first Spring controller.`

*   **Greeting Endpoint (Default):**
    *   URL: `http://localhost:8080/greeting`
    *   Method: `GET`
    *   Response: Renders an HTML page displaying "Hello, World!" and an image.

*   **Greeting Endpoint (Custom Name):**
    *   URL: `http://localhost:8080/greeting?name=YourName`
    *   Method: `GET`
    *   Response: Renders an HTML page displaying "Hello, YourName!" and an image.

## Project Structure

```
.
├── .mvn/
│   └── wrapper/
│       └── maven-wrapper.properties  # Configuration for the Maven Wrapper
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── pl/edu/vistula/first_project_java_spring/
│   │   │       ├── FirstProjectJavaSpringApplication.java # Main application entry point
│   │   │       └── controller/
│   │   │           └── HelloController.java      # Defines web endpoints
│   │   └── resources/
│   │       ├── application.properties          # Spring application configuration
│   │       ├── static/                         # Directory for static assets (CSS, JS, images)
│   │       └── templates/
│   │           └── greeting.html               # Thymeleaf template for the /greeting page
│   └── test/
│       └── ...                                 # Test sources
├── mvnw                                        # Maven Wrapper executable for Unix-like systems
├── mvnw.cmd                                    # Maven Wrapper executable for Windows
└── pom.xml                                     # Maven project configuration (dependencies, build)
