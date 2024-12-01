# Meals-On-Wheels-v1.0

## Meals On Wheels is a platform where users can order meals online, operated by a charitable organization dedicated to providing food services

### Source Code = > 

<a href = 'https://drive.google.com/file/d/1MqR47HW8TQqVKbysZrxfMyuwxTdtjazK/view?usp=sharing'>Click here </a>


## Project Overview

The Know-Your-Neighborhood website consists of the following Key pages

Landing Page /Home Page 
Registration 
Login 
Donation Page 
Contact Us Page 
About Us Page 
Admin Dashboard 
Caregiver Page 
Partner Page 
Member Page
Member Feedback Page 
![image](https://github.com/user-attachments/assets/38ae26f9-e225-4642-9462-7c643bee5afa)


Customers can login using the existing API and fetch basic information such as name, email from API.

## Technologies Used & System Requirements

Backend : Java SE 11, MySQL 8, Spring Boot, Spring Security, OAuth2 (Facebook API), Restful API <br/>
Frontend : React, Tailwindcss, Axios, React-hook-form, React-router-dom <br/>
Tools : Node Js (LTS Ver)

## HOW TO RUN

### Backend

1. **Import Existing Project into Visual Studio Code** <br/>
2. **Create MySQL database**

```bash
mysql> create database kyn
```

3. **Setup application.yml**

```yml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/kyn
    username: <YOUR_DB_USERNAME>
    password: <YOUR_DB_PASSWORD>

  jpa:
    show-sql: true
    hibernate:
      ddl-auto: update
    properties:
      hibernate:
        dialect: org.hibernate.dialect.MySQL8Dialect
  security:
    oauth2:
      client:
        registration:
          facebook:
            clientId: <YOUR_FACEBOOK_CLIENTID>
            clientSecret: <YOUR_FACEBOOK_CLIENTSECRET>
            redirectUri: http://localhost:8080/oauth2/callback/facebook
            scope:
              - email
              - public_profile
        provider:
          facebook:
            authorizationUri: https://www.facebook.com/v3.0/dialog/oauth
            tokenUri: https://graph.facebook.com/v3.0/oauth/access_token
            userInfoUri: https://graph.facebook.com/v3.0/me?fields=id,name,email,picture.width(250).height(250)

app:
  auth:
    tokenSecret: <YOUR_TOKEN_SECRET> (you can go to generator online for token secret)
    tokenExpirationMsec: 86400000
  oauth2:
    authorizedRedirectUris:
      - http://localhost:3000/oauth2/redirect
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

## Screenshot

<p>Home Page</p>
<img src="./Images/Home.png" alt="home_page" width="50%"/>
<p>Register</p>
<img src="./Images/Register.png" alt="register" width="50%"/>
<p>Login</p>
<img src="./Images/Login.png" alt="login" width="50%"/>
<p>Profile page</p>
<img src="./Images/Profile.png" alt="profile" width="50%"/>
<p>Stores</p>
<img src="./Images/SearchStore.png" alt="profile" width="50%"/>
<p>Store Detail</p>
<img src="./Images/ViewStore.png" alt="profile" width="50%"/>
<p>Add Store</p>
<img src="./Images/AddStore.png" alt="profile" width="50%"/>
<p>About Page</p>
<img src="./Images/AboutUs.png" alt="profile" width="50%"/>
<p>Contact Page</p>
<img src="./Images/ContactUs.png" alt="profile" width="50%"/>
<p>Terms and Condition Page</p>
<img src="./Images/Terms.png" alt="profile" width="50%"/>
