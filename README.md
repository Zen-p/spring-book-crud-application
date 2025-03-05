# Spring Boot CRUD Application

REST API for managing books and authors using Spring Boot and PostgreSQL.

## Technologies
- Java 17
- Spring Boot
- PostgreSQL
- Hibernate/JPA
- Docker
- Maven

1. Clone the repository:
```bash
git clone https://github.com/Zen-p/spring-book-crud-application.git
cd spring-book-crud-application
```

2. Build the project:
```bash
mvn clean package
```

3. Start database:
```bash
docker-compose up -d
```

4. Run application
```bash
java -jar target/spring-book-manager-1.0-SNAPSHOT.jar
```

**Done! The application is running.**


API Endpoints

Books
Method	Endpoint	Description
GET	/api/books	Get all books
GET	/api/books/{id}	Get book by ID
POST	/api/books	Create a new book
PATCH	/api/books/{id}	Update a book
DELETE	/api/books/{id}	Delete a book
GET	/api/books/search?title={title}	Search books by title


Authors
Method	Endpoint	Description
GET	/api/authors	Get all authors
GET	/api/authors/{id}	Get author by ID
POST	/api/authors	Create a new author
PATCH	/api/authors/{id}	Update an author
DELETE	/api/authors/{id}	Delete an author


Example Requests

**Create a Book**
```
POST /api/books
Content-Type: application/json
{
  "author": [
    {
      "biography": "Author's biography"
    }
  ],
  "genre": {
    "name": "Science Fiction"
  },
  "yearOfPublication": 2023,
  "description": "Book description",
  "status": true,
  "rating": 5
}
```

Create an Author
```
POST /api/authors
Content-Type: application/json

{
  "biography": "Science fiction author"
}
```


