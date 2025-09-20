# Blog API (Full-Stack Demo) 🚀📝

A small full-stack blog demonstration consisting of an Express JSON API and a simple Express-based frontend.  
This project is designed for learning and quick prototyping: it focuses on clarity and simplicity so you can explore routing, RESTful endpoints, and basic server-rendered views.

## About this project 💡
This repo provides:
- A lightweight API server that exposes typical blog operations (list, read, create, update, delete).
- An Express frontend that consumes the API and renders views (EJS).
- An in-memory data store (no database) so you can run and test quickly.

Intended uses:
- Learning REST API design with Express.
- Demonstrating frontend ↔ backend interaction with server-side rendering.
- Rapid prototyping of blog-like features.

Important notes:
- Data is stored in memory (in the running process). Restarting the API resets all posts.
- Not intended for production use. No authentication, no persistent storage, and minimal validation.
- Recommended as a local dev/demo project or as a starting point for adding persistence and auth.

## Tech stack 🧰
- Node.js (16+)
- Express
- EJS (frontend views)
- body-parser

## Project structure 📁
- index.js — API server (runs on port 4000)
- server.js — Frontend server (renders views on port 3000)
- views/ — EJS templates
- public/ — static assets (CSS, client JS)
- package.json

## Prerequisites ⚙️
- Node.js v16+ installed
- npm available

## Install & run (Windows) ▶️
1. Install dependencies:
```bash
npm install
```

2. Start the API server (port 4000):
```powershell
node index.js
```

3. Start the frontend server (port 3000):
```powershell
node server.js
```

4. Open the frontend in your browser:
http://localhost:3000

## API Endpoints 🔌
Base: http://localhost:4000

- GET /posts — list all posts
- GET /posts/:id — retrieve a single post by id
- POST /posts — create a new post
  - JSON body: { "title": "...", "content": "...", "author": "..." }
- PATCH /posts/:id — partial update (title, content, author)
- DELETE /posts/:id — delete a post

## Quick curl examples 🧪
```bash
# List posts
curl http://localhost:4000/posts

# Get post 1
curl http://localhost:4000/posts/1

# Create a post
curl -X POST http://localhost:4000/posts -H "Content-Type: application/json" -d "{\"title\":\"Hi\",\"content\":\"Hello\",\"author\":\"You\"}"
```

## Screenshots 📸
<img width="1002" height="857" alt="1" src="https://github.com/user-attachments/assets/1cf022fd-9b6c-4c57-8736-7acafd5c6e0b" />


## Development tips 🛠️
- Add validations before pushing to production (title/content length, required fields).
- Replace in-memory store with a database (SQLite/Postgres/Mongo) to persist data.
- Add authentication (JWT, sessions) and authorization for create/update/delete operations.
- Add tests (e.g., Jest + supertest) for API endpoints.

## Contributing 🤝
Feel free to open issues or submit PRs to:
- Add persistence
- Improve validation and error handling
- Add tests or CI

## License & Contact 📬
This demo is provided as-is for learning and prototyping. No license specified, add one if you plan to publish.  
Questions or improvements: open an issue or submit a PR on your
