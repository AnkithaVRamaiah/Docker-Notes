# Writing Dockerfiles for Different Applications: Python Flask, Node.js Express, and Java Spring Boot


### 1. **Python Flask Application**

#### Code and Dependencies
**`app.py`:**
```python
from flask import Flask
app = Flask(__name__)

@app.route('/')
def home():
    return "Hello, Flask!"

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000)
```

**`requirements.txt`:**
```
Flask==2.0.3
```

#### Dockerfile
```Dockerfile
# Use the official Python image as the base
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file to the container
COPY requirements.txt .

# Install the dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the current directory contents into the container
COPY . .

# Expose port 5000
EXPOSE 5000

# Run the application
CMD ["python", "app.py"]
```

### 2. **Node.js Express Application**

#### Code and Dependencies
**`app.js`:**
```javascript
const express = require('express');
const app = express();
const port = 3000;

app.get('/', (req, res) => {
  res.send('Hello, Express!');
});

app.listen(port, () => {
  console.log(`App listening at http://localhost:${port}`);
});
```

**`package.json`:**
```json
{
  "name": "express-app",
  "version": "1.0.0",
  "main": "app.js",
  "dependencies": {
    "express": "^4.17.1"
  },
  "scripts": {
    "start": "node app.js"
  }
}
```

#### Dockerfile
```Dockerfile
# Use the official Node.js image as the base
FROM node:14

# Set the working directory
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install the dependencies
RUN npm install

# Copy the rest of the application
COPY . .

# Expose port 3000
EXPOSE 3000

# Run the application
CMD ["npm", "start"]
```

### 3. **Java Spring Boot Application**

#### Code and Dependencies
**`Application.java` (inside `src/main/java/com/example/demo`):**
```java
package com.example.demo;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@SpringBootApplication
@RestController
public class Application {

    public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
    }

    @GetMapping("/")
    public String home() {
        return "Hello, Spring Boot!";
    }
}
```

**`pom.xml`:**
```xml
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>
    <groupId>com.example</groupId>
    <artifactId>demo</artifactId>
    <version>1.0.0</version>
    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>2.5.5</version>
    </parent>
    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
    </dependencies>
</project>
```

#### Dockerfile
```Dockerfile
# Use Maven to build the application
FROM maven:3.8.5-openjdk-11 AS build
WORKDIR /app
COPY pom.xml .
COPY src ./src
RUN mvn package -DskipTests

# Use OpenJDK to run the application
FROM openjdk:11-jre-slim
WORKDIR /app
COPY --from=build /app/target/demo-1.0.0.jar app.jar
EXPOSE 8080
CMD ["java", "-jar", "app.jar"]
```

### Industry Context
- **Dependencies Management:** In real projects, dependencies are managed using files like `requirements.txt` for Python, `package.json` for Node.js, and `pom.xml` for Java.
- **Build Steps:** Java applications often require a build step using Maven or Gradle, which is reflected in the multi-stage Dockerfile.
- **Port Exposure:** Identifying the correct ports to expose is crucial for container communication.
- **Base Images:** Choosing the right base image for efficiency and compatibility.

