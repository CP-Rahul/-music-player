# MUSIC PLAYER

## Description
This is an music player web app using the MERN stack (MongoDB, Express, React, Node.js). The app allows users to sign up, sign in, select songs from a library, create playlists, play songs, and resume songs from where they left off.

## Setup the project

- Download project from github and open it in your favourite text editor.

### Requirements

- Node.js (v12 or higher)
- MongoDB

### backend

- Go inside the backend folder and execute the following command:

```
npm install
```

- In the root directory create a `.env` file and add the following env variables
  example:
  ```
      PORT=3000
      SALT=8
      JWTSECRET='mysecret'
      JWTEXPIRY='1h'
      PORT=3000
      SALT=8
      JWTEXPIRY='1d'
      JWTSECRET='JWT'
      MONGOURL='mongodburl'
  ```

- To run the client execute

```
npm start
```

### frontend

- Go inside the frontend folder and execute the following command:

```
npm install
```

- In the root directory create a `.env` file and add the following env variables
  example:
  ```
    baseUrl=backendUrl/api/v1
  ```

- To run the client execute

```
npm run dev
```
### Folder Structure - Backend

`src` -> Inside the src folder all the actual source code regarding the project will reside, this will not include any kind of tests.

Lets take a look inside the `src` folder

 - `config` -> In this folder anything and everything regarding any configurations or setup of a library or module will be done. For example: setting up `dotenv` so that we can use the environment variables anywhere in a cleaner fashion, this is done in the `server-config.js`. One more example can be to setup you logging library that can help you to prepare meaningful logs, so configuration for this library should also be done here. 

 - `routes` -> In the routes folder, we register a route and the corresponding middleware and controllers to it. 

 - `middlewares` -> they are just going to intercept the incoming requests where we can write our validators, authenticators etc. 

 - `controllers` -> they are kind of the last middlewares as post them you call you business layer to execute the budiness logic. In controllers we just receive the incoming requests and data and then pass it to the business layer, and once business layer returns an output, we structure the API response in controllers and send the output. 

 - `repositories` -> this folder contains all the logic using which we interact the DB by writing queries, all the raw queries or ORM queries will go here.

 - `services` -> contains the buiness logic and interacts with repositories for data from the database

 - `utils` -> contains helper methods, error classes etc.

 - `public` -> contains the static files.

 ### Folder Structure - Frontend

 `src` -> Inside the src folder all the actual source code regarding the project will reside, this will not include any kind of tests.

Lets take a look inside the `src` folder

 - `components` -> This folder contains all the reusable UI components.
 - `constants` -> contains constant variables.
 - `hooks` -> contains custom hooks'.
 - `redux` -> contains all Redux-related code for state management.
 - `utils` -> contains helper methods and constant etc.
