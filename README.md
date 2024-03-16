# SpringStudents

This project was designed to familiarize you with Spring Boot. Spring Boot makes it easy to create stand-alone, production-grade Spring based Applications that you can "just run".

This application manages student information and also stores this information in a database. The controller that handles incoming requests from outside has 4 access points:

**GET** to retrieve a student by their email or all students stored in the database at once.

**POST** to store the students in the database.

**PUT** is needed to update the already existing student records.

**DELETE** is used to delete a student by their email.

The application is built on a three-tier architecture: controller, service, repository. It doesn't matter which device the API is used from, as everything is supported.

Two services are also implemented: the first service stores students in the application memory and the second service that stores students in a PostgreSQL database. You can switch between these two implementations using annotations.

This application is a good example of how Spring is able to handle queries: from initial query input, finding the right checkpoint and the right execution method, to going to the database and sending the response to the end user.
## Features

- All CRUD operations are represented
- Using the Lombok library
- Representation of various annotations
- Cross platform

## Database

Table *students* with columns:
| Column name | Type | Key | Null |
| :-------- | :------------------------- | :-------- | :-------- |
| id | bigint | PRIMARY KEY | NOT NULL |
| first_name | character varying (255) | - | NULL |
| last_name | character varying (255) | - | NULL |
| email | character varying (255) | UNIQUE | NULL |
| date_of_birth | date | - | NULL |

## API Reference

#### Get all students

```http
  localhost:8080/api/v1/students
```

#### Get a certain student

```http
  localhost:8080/api/v1/students/random123@yahoo.com
```

#### Save student

```http
  localhost:8080/api/v1/students/save_student
```

| Response | Output |
| :-------- | :------------------------- |
| `200` | Student: successfully saved! |

#### Update student

```http
  localhost:8080/api/v1/students/update_student
```
#### Delete student (a random email example)

```http
  localhost:8080/api/v1/students/delete_student/random123@yahoo.com
```

## 🔗 Links
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anna-porumbescu-4bb452229/)
