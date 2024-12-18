# Meals-On-Wheels-v1.0

## Meals On Wheels is a platform where users can order meals online, operated by a charitable organization dedicated to providing food services

### Source Code = > 

<a href = 'https://drive.google.com/file/d/1MqR47HW8TQqVKbysZrxfMyuwxTdtjazK/view?usp=sharing'>Click here </a>


## Project Overview

The Meals On Wheels website consists of the following Key pages

1. Landing Page /Home Page 
2. Registration 
3. Login 
4. Donation Page
5. Contact Us Page 
6. About Us Page 
7. Admin Dashboard 
8. Caregiver Page 
9. Partner Page 
10. Member Page
11. Member Feedback Page 

Roles are,

1. Member
2. Caregiver
3. Rider
4. Partner
5. Admin
6. Volunteer

## Technologies Used & System Requirements

We will develop the project containing all the points in our notes. Our main focus will be making the ordering and delivery procedure simple for the aged, diseased, or disabled customer as well as for the business. Besides the system should be user-friendly with a dynamic menu, so that all the options can be easily visible. 
The application will be developed using Spring Security for the backend, Restful Web Services for API, and React JS for the front end. Throughout the project development period, the adaptive software development method will be followed

## HOW TO RUN

### Backend

1. **Import Existing Project into Visual Studio Code** <br/>
2. **Create MySQL database**

```bash
mysql> create database mom
```

3. **Setup application.properties**

```yml
spring.datasource.url= jdbc:mysql://localhost:3306/mom?useSSL=false
spring.datasource.username= <username>
spring.datasource.password= <password>

spring.jpa.properties.hibernate.dialect= org.hibernate.dialect.MySQL5InnoDBDialect
spring.jpa.hibernate.ddl-auto= update

# App Properties
mow.app.jwtSecret= group2SecretKey
mow.app.jwtExpirationMs= 86400000

## MULTIPART (MultipartProperties)
# Enable multipart uploads
spring.servlet.multipart.enabled=true
# Threshold after which files are written to disk.
spring.servlet.multipart.file-size-threshold=2KB
# Max file size.
spring.servlet.multipart.max-file-size=200MB
# Max Request Size
spring.servlet.multipart.max-request-size=215MB

## File Storage Properties
# Please change this to the path where you want the uploaded files to be stored.
file.upload-dir=./src/main/resources/images

    
```

4. **Get Client ID & Client Secret Facebook API**

- <a href="https://developers.facebook.com/docs/facebook-login/">Facebook Docs to create Facebook Login endpoint API</a>

5. **Run Java Application**

### Frontend

1. **Import existing project to your Text Editor/IDE and run NPM Install**

```bash
npm install
```

2. **Run React application with NPM Start (Make sure the backend is also running in the localhost:8080)**

```bash
npm start
```

3. **Open [http://localhost:3000](http://localhost:3000) to view it in the browser.**

