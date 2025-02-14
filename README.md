# MongoDB Setup and Usage Guide

MongoDB is a NoSQL database known for its scalability, flexibility, and document-oriented structure. It stores data in JSON-like BSON format and is widely used in modern web applications.

---

## 📌 Step 1: Install MongoDB on Windows

### 🔹 Windows Installation:
1. Download MongoDB Community Server from the [MongoDB Download Center](https://www.mongodb.com/try/download/community).
2. Run the installer and select **Complete Setup**.
3. Ensure you check **"Install MongoDB as a service"** for automatic startup.
4. Add MongoDB binaries to the system `PATH`:
   - Open **System Properties** → **Advanced** → **Environment Variables**.
   - Under **System Variables**, edit the `Path` variable and add:
     ```
     C:\Program Files\MongoDB\Server\<version>\bin
     ```
5. Verify installation by running:
   ```sh
   mongod --version
   ```

---

## 📌 Step 2: Install MongoDB Shell (mongosh)
`mongosh` is the interactive command-line shell for MongoDB.

### 🔹 Installation:
- Download `mongosh` from the [MongoDB Download Center](https://www.mongodb.com/try/download/shell).
- Install and verify using:
  ```sh
  mongosh --version
  ```

---

## 📌 Step 3: Start and Connect to MongoDB
### 🔹 Start MongoDB Server:
1. Open Command Prompt and start the MongoDB server:
   ```sh
   mongod
   ```

### 🔹 Connect to MongoDB:
2. In another terminal, connect to the database:
   ```sh
   mongosh
   ```

---

## 📌 Step 4: Insert and Query Data
### 🔹 Insert Data into a Collection:
```sh
use myDatabase

db.books.insertMany([
  {
    "title": "The Pragmatic Programmer",
    "author": "Andrew Hunt, David Thomas",
    "publishedYear": 1999,
    "genre": "Technology",
    "ISBN": "978-0201616224"
  },
  {
    "title": "Clean Code",
    "author": "Robert C. Martin",
    "publishedYear": 2008,
    "genre": "Technology",
    "ISBN": "978-0132350884"
  }
])
```

### 🔹 Query Data:
```sh
db.books.find().pretty()
```

---

## 📌 Step 5: Stop MongoDB
- Stop the MongoDB service:
  ```sh
  net stop MongoDB
  ```

---

## 🎯 Conclusion
You have successfully installed, set up, and used MongoDB on Windows! 🎉 Happy coding!

---

## 🚀 How to Upload to GitHub
1. Initialize a new Git repository:
   ```sh
   git init
   ```
2. Add the README file:
   ```sh
   git add README.md
   ```
3. Commit the changes:
   ```sh
   git commit -m "Added MongoDB setup guide"
   ```
4. Add the remote repository:
   ```sh
   git remote add origin <your-github-repo-url>
   ```
5. Push to GitHub:
   ```sh
   git push -u origin main
   ```

---

✅ Now your MongoDB setup guide is ready for GitHub! 🚀

