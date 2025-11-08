🧠 Mongoose Checkpoint Project
📌 Overview

This project demonstrates how to connect a Node.js application to a MongoDB Atlas database using Mongoose, define a schema, and perform basic CRUD (Create, Read, Update, Delete) operations.
It also includes a series of guided tests to confirm correct functionality.

⚙️ Features Implemented

The project covers the following Mongoose operations:

Step	Operation	Description
1️⃣	Connection Setup	Connects to MongoDB Atlas using mongoose.connect() and .env configuration
2️⃣	Schema & Model	Defines a Person schema with name, age, and favoriteFoods
3️⃣	Create One	Creates and saves a single Person document
4️⃣	Create Many	Inserts multiple people at once using Model.create()
5️⃣	Find by Name	Uses Model.find() to search for all people with a given name
6️⃣	Find One by Food	Uses Model.findOne() to find one person by their favorite food
7️⃣	Find by ID	Uses Model.findById() to locate a person by _id
8️⃣	Find, Edit, Then Save	Updates a person’s favoriteFoods array, then saves the changes
9️⃣	Find One and Update	Updates a person’s age using findOneAndUpdate()
🔟	Delete Operations	Removes one person by ID and deletes all people named “Mary”
⚡	Query Chaining	Combines .find(), .sort(), .limit(), .select(), and .exec()
🧰 Technologies Used

Node.js v22+

Mongoose (ODM for MongoDB)

MongoDB Atlas (Cloud Database)

dotenv (for environment variable management)

🗂️ Project Structure
mongoose-checkpoint/
│
├── node_modules/
├── .env
├── package.json
├── test.js
├── mongooseCheckpoint.js
└── README.md

⚡ Setup and Usage
1. Clone or create the project
git clone <your_repo_url>
cd mongoose-checkpoint

2. Install dependencies
npm install

3. Create .env file

Create a file named .env in the project root and add your MongoDB Atlas connection string:

MONGO_URI='your_atlas_connection_string_here'


⚠️ Important: Do not include spaces around the = sign and keep your credentials private.

4. Run the tests
npm test


You should see output similar to this:

=== Starting Mongoose Tests ===
✅ All tests completed successfully!
✅ Database connection closed.

📄 Example Schema
const personSchema = new mongoose.Schema({
  name: { type: String, required: true },
  age: Number,
  favoriteFoods: [String],
});

💡 Notes

Ensure your MongoDB Atlas cluster is accessible (IP whitelisted or set to 0.0.0.0/0 for testing).

Always commit your code without the .env file for security reasons.

The project uses callback functions following the Node.js convention (err, data).

👩🏽‍💻 Author

Anna Muoki
📍 Nairobi, Kenya
💬 Passionate about technology, education, and community impact.

🏁 License

This project is open-source and available for educational purposes only.
