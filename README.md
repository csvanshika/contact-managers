# contact-managers"name": "server",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "nodemon src/server.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "type": "module",
  "dependencies": {
    "bcryptjs": "^3.0.3",
    "compress-json": "^3.4.0",
    "cors": "^2.8.6",
    "dotenv": "^17.3.1",
    "express": "^5.2.1",
    "express-validator": "^7.3.1",
    "jsonwebtoken": "^9.0.3",
    "mongoose": "^9.2.1",
    "nodemon": "^3.1.11"
  }
}
import Contact from '../models/Contact.js';


Installation
Clone the repository

git clone https://github.com/Mayankkumar1234/My-LibSpace
cd My-LibSpace
Install dependencies

[e.g., npm install]
Configure Environment Variables

Create a .env file in the root directory.
Add the following variables :
MONGO_URI=your_database_url
PORT = Your server port
SECRET_KEY= For JWT
Run the application

npm run start or node index.js


