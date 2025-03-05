```
📚 Spring Boot CRUD Application - Book & Author Management

A RESTful API for managing books and authors built with Spring Boot and PostgreSQL.  
Deployable via Docker with full CRUD operations and search capabilities.

---

🛠 Technologies:
- Java 17 
- Spring Boot 3 
- PostgreSQL
- Hibernate/JPA 
- Docker
- Maven

---

🚀 Getting Started:

1. Clone Repository:
git clone https://github.com/Zen-p/spring-book-crud-application.git
cd spring-book-crud-application

2. Build Project:
mvn clean package

3. Start Database & pgAdmin:
docker-compose up -d

4. Run Application:
java -jar target/spring-book-manager-1.0-SNAPSHOT.jar

Success! Application running at http://localhost:8080

---

🔍 API Endpoints:

📖 Books API:
GET     /api/books              - Get all books
GET     /api/books/{id}         - Get book by ID
POST    /api/books              - Create new book
PATCH   /api/books/{id}         - Update book (partial update)
DELETE  /api/books/{id}         - Delete book
GET     /api/books/search?title={title} - Search books by title

✍️ Authors API:
GET     /api/authors            - Get all authors
GET     /api/authors/{id}       - Get author by ID
POST    /api/authors            - Create new author
PATCH   /api/authors/{id}       - Update author (partial update)
DELETE  /api/authors/{id}       - Delete author

---

📄 Example Requests:

Create Book:
POST /api/books
Content-Type: application/json

{
  "author": [{
    "biography": "Renowned sci-fi writer"
  }],
  "genre": {
    "name": "Science Fiction"
  },
  "yearOfPublication": 2023,
  "description": "Epic space adventure",
  "status": true,
  "rating": 5
}

Create Author:
POST /api/authors
Content-Type: application/json

{
  "biography": "Pioneer of cyberpunk literature"
}

---

⚙️ Environment Setup:

🐘 PostgreSQL Configuration:
Host:       localhost
Port:       5432
Database:   postgres
User:       postgres
Password:   postgres

📊 pgAdmin Access:
URL:        http://localhost:5050
Email:      admin@admin.com
Password:   admin

Tip: Use Postman or curl to test API endpoints after starting the application!
```
