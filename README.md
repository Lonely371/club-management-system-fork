# club-management-system
[ Group project for CMPT354 Database Systems I ]
- Design a user-centric, responsive UI for the club platform using Vue and Ant Design, focusing on usability to enhance engagement and member satisfaction.
- Utilized Spring Boot and Spring MVC to construct the backend framework; Built and managed dependencies of the project by Maven, and designed the database access object and service layer to facilitates interaction between the controller and database.
- Modernize outdated JDBC data handling system by integrating Hibernate with MySQL, resulting in notable improvements in system performance and reliability.

# Development Environment

- JDK 17
- SpringBoot 2.7.17
- Maven 3.6.1
- Node.js 18.16.0
- @vue/cli 5.0.8
- MySQL 8.1.0

# Get Started
### `vue setup`
Change your current working directory to the **vue** folder:
```bash
cd vue
```

then:
```
npm install
```

### `Compiles and hot-reloads for development`
```
npm run serve
```

### `Compiles and minifies for production`
```
npm run build
```

### `Customize configuration`
See [Configuration Reference](https://cli.vuejs.org/config/).

# Database Configuration
To establish the database connection using the default configuration in the **application.yml** file located in the **src\main\resources** directory, please follow the steps outlined below:

1. Create a local MySQL database

Begin by creating a new database named club. This database will be used for managing user data. You can create the database using the following SQL command:
```
CREATE DATABASE club;
```
2. Create the sys_user table

With the club database selected, execute the following SQL command to create a sys_user table. This table will store user information with various attributes such as username, password, and contact details.

```
CREATE TABLE sys_user (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50),
    password VARCHAR(50),
    nickname VARCHAR(50),
    email VARCHAR(50),
    phone VARCHAR(20),
    address VARCHAR(255),
    create_time TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    avatar_url VARCHAR(50)
);
```
3. Connect to the database

Ensure that your application.yml contains the correct database connection settings corresponding to the database club. Update the credentials if necessary to match your local MySQL setup.

# Contributing
If you want to contribute to this project, please fork this repository and create a pull request, or drop me an email at kha112@sfu.ca
