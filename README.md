# Fiverr Clone Backend

This is a Node.js backend for a Fiverr-like freelance marketplace. It provides RESTful APIs for user authentication, gig management, messaging, orders, reviews, and more.

## Features

- User registration, login, and authentication (JWT)
- Create, update, delete gigs
- Messaging between users
- Order management
- Review system
- Secure API endpoints

## Technologies Used

- Node.js
- Express.js
- MongoDB (Mongoose)
- JWT for authentication

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v14 or higher recommended)
- [MongoDB](https://www.mongodb.com/)

### Installation

1. **Clone the repository:**
   ```powershell
   git clone https://github.com/alwaysjeevanr/Fiverr-Clone-Backend.git
   cd Fiverr-Clone-Backend/server
   ```
2. **Install dependencies:**
   ```powershell
   npm install
   ```
3. **Configure environment variables:**
   - Create a `.env` file in the `server` directory.
   - Add the following variables:
     ```env
     MONGO_URI=your_mongodb_connection_string
     JWT_SECRET=your_jwt_secret
     PORT=5000
     ```

### Running the Server

```powershell
node server.js
```

The server will start on the port specified in your `.env` file (default: 5000).

## API Endpoints

### Authentication

- `POST /api/auth/register` — Register a new user
- `POST /api/auth/login` — Login and receive JWT

### Gigs

- `GET /api/gigs` — List all gigs
- `POST /api/gigs` — Create a new gig
- `PUT /api/gigs/:id` — Update a gig
- `DELETE /api/gigs/:id` — Delete a gig

### Orders

- `GET /api/orders` — List orders
- `POST /api/orders` — Create an order

### Messages

- `GET /api/messages/:conversationId` — Get messages in a conversation
- `POST /api/messages` — Send a message

### Reviews

- `GET /api/reviews/:gigId` — Get reviews for a gig
- `POST /api/reviews` — Add a review

### Users

- `GET /api/users/:id` — Get user profile
- `PUT /api/users/:id` — Update user profile

## Folder Structure

```
server/
  controllers/    # Route handlers
  middleware/     # JWT and other middleware
  models/         # Mongoose models
  routes/         # API route definitions
  utils/          # Utility functions
  server.js       # Entry point
  package.json    # Dependencies
```

## Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License.
