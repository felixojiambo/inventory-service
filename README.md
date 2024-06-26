Inventory Service

Overview

The Inventory Service is a RESTful web service designed to manage inventory information for an e-commerce platform. It provides an API endpoint to check the stock availability of products based on their SKU codes. The service is built using Spring Boot, a popular framework for building Java-based web applications.

Features

- Inventory Check: Allows checking the stock availability of products by their SKU codes.
- RESTful API: Provides a simple and intuitive API for interacting with the inventory data.
- Logging: Utilizes SLF4J for logging, ensuring that all important operations and errors are recorded.
- Transactional Operations: Ensures data integrity and consistency by performing database operations within transactions.

Getting Started

Prerequisites

- Java 17 or higher
- Maven 3.10 or higher
- A relational database (e.g., MySQL, PostgreSQL)

Building the Project

1. Clone the repository to your local machine.
2. Navigate to the project directory.
3. Run the following Maven command to build the project:
   ```
   mvn clean install
   ```
4. After the build is successful, you can start the application by running:
   ```
   java -jar target/inventory-service-0.0.1-SNAPSHOT.jar
   ```

Configuration

The application uses Spring Boot's application.properties file for configuration. You will need to specify the database connection details in this file.

API Documentation

Endpoint

-GET /api/inventory: Checks the stock availability of products by their SKU codes.

Parameters

- `skuCode`: A list of SKU codes to check.

Response

- A list of `InventoryResponse` objects, each containing the SKU code and a boolean indicating whether the product is in stock.

Example Request

```
GET /api/inventory?skuCode=SKU123&skuCode=SKU456
```

Example Response

```json
[
    {
        "skuCode": "SKU123",
        "isInStock": true
    },
    {
        "skuCode": "SKU456",
        "isInStock": false
    }
]
```

Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue if you find any bugs or have suggestions for improvements.

License

This project is licensed under the MIT License. See the LICENSE file for details.
