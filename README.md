# Proofd

**_A blockchain enabled verification platform_**

Proofd allows users to securely proof data such as important documents on the blockchain. After logging in, users can connect with third party applications, such as DocuSign, and put data such as signed legal documents, on the Bitcoin blockchain for secure, immutable proof of the transaction.

### Stack

Proofd utilizes [Heroku](https://www.heroku.com/) and [Netlify](https://www.netlify.com/) for deployment, and is built in full stack JavaScript with a [React.js](https://reactjs.org/) frontend, [Node.js](https://nodejs.org/en/)/[Express.js](https://expressjs.com/) backend, and a [PostgreSQL](https://www.postgresql.org) database in production, while a [SQLite3](https://www.sqlite.org/index.html) database was used in development.

### Frontend

[https://chainpoint-docusign.netlify.com/](https://chainpoint-docusign.netlify.com/)

The frontend of Proofd utilizes React, Redux for state management, React-Router, and axios for making our API calls, as well as Auth0 for authentication, with both local, and social login availability.

### Backend

[https://chainpoint-docusign-server.herokuapp.com/](https://chainpoint-docusign-server.herokuapp.com/)

Our backend consists of Node.js, Express.js, and utilizes the Chainpoint API for connecting to the blockchain, as well as Stripe for payment processing.

### API Endpoints

| Method | Endpoint                | Request               | Response                                             |
| ------ | ----------------------- | --------------------- | ---------------------------------------------------- |
| GET    | /users/profile          |                       | Object of logged in user.                            |
| GET    | /users/subscription     | email\*               | Object with subscription type and remaining credits. |
| PUT    | /users/image            | uploaded_picture\*    | Count of updated users.                              |
| GET    | /documents              | id\*                  | Single document object.                              |
| GET    | /envelopes/all          | user                  | Array of Envelopes                                   |
| GET    | /payment                |                       | Array of Invoice objects                             |
| GET    | /payment/:id            | id\*                  | Single Invoice Object                                |
| POST   | /payment                | userId, stripeCharges | Invoice                                              |
| GET    | /chainpoint/:id         | id\*                  | Object with document status                          |
| GET    | /chainpoint/:id/loading | id\*                  | Object with envelope status                          |
| GET    | /auth/logout            |                       | 200 on successful logout                             |

\* denotes required field.

## The Proofd Team

- [Brandon Aguirre](https://github.com/DirupT)
- [Randy Calderon](https://github.com/RandyCalderon)
- [Sean Chavez](https://github.com/seanchavez)
- [Zack Hitchcock](https://github.com/zackhitch)
- [Jeremy Jones](https://github.com/crypto-jones)
- Shoutout to [Jared Cuffe](https://github.com/jcuffe)
