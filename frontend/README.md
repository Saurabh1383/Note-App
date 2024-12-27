# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

#Introduction
A web application with CRUD (Create, Retrieve, Update, Delete) functionality built using MERN stack (MongoDB, Express, React, Node.js) that allows the user to view, create, update and delete notes in the form of visual cards.

#Tech stacks used
MongoDB - For database functionality
Express - For handling server side (backend) functions
React - For frontend and client side functions
Node.js - For backend functions

#Backend
#General
Express routers are used to handle user and note functions.
Mongoose is used to handle MongoDB connection.

#Authentication
HTTP POST requests are used for both sign up and log in.
Signing up requires creating a username, entering email and password.
Uses bcrypt to encrypt passwords given by users before storing them in database.
Before sign up, the API checks DB to ensure email does not already exist.
For logging in, DB is checked to make sure user exists.
Then a JWT token is created after signing the payload (the user ID in the database) with a secret key and given an expiration time of 1 day.
After successful login, this token is returned.
For every operation involving notes, this token is sent in the appropriate HTTP request's header.
If token expires, user is requested to login again.

● Steps to set up and run the application locally.

1. Open the code in the VS Code
2. Install the npm in both file in backed or frontend
3. Run the project locally through command npm run dev
4. Connect the database to the mongodb to collecting the data from the user
5. Check the thunder client api so that data is coming or not
6. Now you can go to the frontend part for login and signup
