# Blog Application API

REST API built with Node.js, Express, MongoDB, and bcrypt.

## Setup
//Download Zip from here
```bash
npm install
```

Create a `.env` file:
```
MONGO_URI=(your-MongoDB-URL-Here)
PORT=3000
```

```bash
npm start
```

## API Endpoints

### Users
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /api/users/register | Register new user |
| GET | /api/users | Get all users |
| GET | /api/users/:id | Get user + their posts |

### Posts
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /api/posts | Create post |
| GET | /api/posts | Get all posts with author |
| GET | /api/posts/:id | Get post with comments |
| GET | /api/posts/tag/:tag | Get posts by tag |
| PUT | /api/posts/:id | Update post |
| DELETE | /api/posts/:id | Delete post + comments |

### Comments
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /api/posts/:postId/comments | Add comment |
| GET | /api/posts/:postId/comments | Get post comments |
| DELETE | /api/comments/:id | Delete comment |

## Sample Request Bodies

**Register User:**
```json
{
  "username": "Husnain",
  "email": "husnain@example.com",
  "password": "secret123"
}
```

**Create Post:**
```json
{
  "title": "Getting Started with REST APIs",
  "content": "REST stands for Representational State Transfer...",
  "author": "65f1a2b8c9d4e5f6a7b8c9d0",
  "tags": ["nodejs", "express", "mongodb"]
}
```

**Add Comment:**
```json
{
  "text": "Great post!",
  "user": "65f1a2b8c9d4e5f6a7b8c9d0"
}
```
