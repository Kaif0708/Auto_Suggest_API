# Auto Suggest API

## Overview

This project is an Auto Suggest API built using Spring Boot, Maven, and Elasticsearch. The API provides suggestions based on partial user inputs, making it easier to search and find relevant data.

## Features

- **Auto Suggestion**: Provides real-time suggestions based on user input.
- **Elasticsearch Integration**: Utilizes Elasticsearch for efficient and scalable search capabilities.
- **RESTful API**: Exposes endpoints for interaction with the auto-suggest feature.

## Prerequisites

- **Java 11 or higher**
- **Maven 3.6 or higher**
- **Elasticsearch 7.x or higher**
- **Spring Boot 2.5 or higher**

## Setup Instructions

### Clone the Repository

```bash
git clone https://github.com/yourusername/auto-suggest-api.git
cd auto-suggest-api
```

### Elasticsearch Setup

1. Download and install Elasticsearch from the [official website](https://www.elastic.co/downloads/elasticsearch).
2. Start Elasticsearch:

```bash
./bin/elasticsearch
```

### Configure Elasticsearch

Update the `application.properties` file with your Elasticsearch configuration:

```properties
spring.elasticsearch.rest.uris=http://localhost:9200
```

### Build and Run the Application

1. Build the project using Maven:

```bash
mvn clean install
```

2. Run the Spring Boot application:

```bash
mvn spring-boot:run
```

## API Endpoints

### Suggest API

- **Endpoint**: `/api/suggest`
- **Method**: `GET`
- **Description**: Provides suggestions based on the input query.
- **Parameters**:
  - `query` (required): The partial input text for suggestions.
- **Example Request**:

```bash
curl -X GET "http://localhost:8080/api/suggest?query=example"
```

### Example Response

```json
{
  "suggestions": [
    "example1",
    "example2",
    "example3"
  ]
}
```

## Dependencies

The project uses the following dependencies:

- **Spring Boot Starter Web**: For building RESTful web applications.
- **Spring Boot Starter Data Elasticsearch**: For integrating Elasticsearch with Spring Boot.
- **Spring Boot Starter Test**: For testing the application.
