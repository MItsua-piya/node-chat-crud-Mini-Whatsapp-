# 💬 Mini WhatsApp – Node Chat CRUD

A simple chat application built with **Node.js, Express, MongoDB and EJS**. It demonstrates full **CRUD** (Create, Read, Update, Delete) operations on chat messages, with a clean WhatsApp-style interface.

---

## ✨ Features

- 📋 **View** all chats in a WhatsApp-like layout
- ➕ **Create** a new chat message (sender, receiver, message)
- ✏️ **Edit** an existing message
- 🗑️ **Delete** a message
- 🕒 Each chat is stored with a timestamp
- 🌱 Seed script (`init.js`) to fill the database with sample chats

---

## 🛠️ Tech Stack

| Layer      | Technology                     |
| ---------- | ------------------------------ |
| Runtime    | Node.js                        |
| Server     | Express 5                      |
| Database   | MongoDB with Mongoose          |
| Templating | EJS                            |
| HTTP verbs | method-override (PUT / DELETE) |

---

## 📁 Project Structure

```
node-chat-crud-Mini-Whatsapp-/
├── models/          # Mongoose schemas (Chat model)
├── public/          # Static files (CSS, client-side assets)
├── views/           # EJS templates
├── index.js         # Express app, routes and server entry point
├── init.js          # Script to seed the database with sample chats
├── package.json
└── .gitignore
```

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or later recommended)
- [MongoDB](https://www.mongodb.com/try/download/community) running locally (default: `mongodb://127.0.0.1:27017`)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/MItsua-piya/node-chat-crud-Mini-Whatsapp-.git

# 2. Move into the project folder
cd node-chat-crud-Mini-Whatsapp-

# 3. Install dependencies
npm install
```

### Seed the database (optional)

```bash
node init.js
```

### Run the app

```bash
node index.js
```

Then open your browser and visit:

```
http://localhost:8080/chats
```

> The port and route may differ depending on your `index.js`. Check the `app.listen(...)` line to confirm.

---

## 🔄 CRUD Operations

| Operation | Method   | Route (typical)    | Description                |
| --------- | -------- | ------------------ | -------------------------- |
| Read      | `GET`    | `/chats`           | Show all chats             |
| Create    | `GET`    | `/chats/new`       | Form to create a chat      |
| Create    | `POST`   | `/chats`           | Save a new chat            |
| Update    | `GET`    | `/chats/:id/edit`  | Form to edit a chat        |
| Update    | `PUT`    | `/chats/:id`       | Update the chat message    |
| Delete    | `DELETE` | `/chats/:id`       | Delete a chat              |

---

## 🧩 Chat Schema

```js
{
  from:       String,   // sender
  to:         String,   // receiver
  msg:        String,   // message text
  created_at: Date      // timestamp
}
```

---

## 📸 Screenshots

_Add screenshots of your app here._

```md
![Home Page](./screenshots/home.png)
```

---

## 🤝 Contributing

Contributions, issues and feature requests are welcome!

1. Fork the project
2. Create your feature branch: `git checkout -b feature/my-feature`
3. Commit your changes: `git commit -m "Add my feature"`
4. Push to the branch: `git push origin feature/my-feature`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **ISC License**.

---

## 👤 Author

**MItsua-piya** – [GitHub Profile](https://github.com/MItsua-piya)

⭐ If you found this project helpful, consider giving it a star!
