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



// @desc    Get all contacts for logged-in user

// @route   GET /api/contacts

// @access  Private

const getContacts = async (req, res) => {

  try {

    const contacts = await Contact.find({ userId: req.user._id }).sort({

      createdAt: -1,

    });



    res.json({ success: true, count: contacts.length, contacts });

  } catch (error) {

    res.status(500).json({ message: error.message });

  }

};
