# Flag Quiz Game

This project is a simple quiz application that challenges users to guess the country name based on flags. The application uses an Express.js server, connects to a PostgreSQL database for storing country flags, and renders the front-end using EJS templates.

## Features

- Displays a flag from the database and prompts the user to guess the country name.
- Tracks the user's score throughout the session.
- Provides feedback on whether the answer was correct or incorrect.
- Renders the score and allows users to restart the game after each incorrect answer.

## Setup

### Prerequisites

- Node.js (version 14 or later)
- PostgreSQL

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/flag-quiz-game.git
   cd flag-quiz-game
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Set up your PostgreSQL database:
   - Create a PostgreSQL database named world.
   - Create a table named flags with columns for the country name and flag URL.
   - Example SQL command to create the table:
     ```bash
     CREATE TABLE flags (
      id SERIAL PRIMARY KEY,
      country VARCHAR(100),
      flag VARCHAR(255)
     );
     ```
4. opulate the flags table with data (country name and flag image URLs).
5. Create a .env file in the root directory and add your PostgreSQL credentials:
   ```bash
   DB_PASSWORD=your_database_password
   ```
6. Update the DB_PASSWORD in .env with your actual PostgreSQL password.
7. Starting the Server
```bash
node index.js
```

## Application Structure
- index.js: The main application logic, including routes and database connections.
- index.ejs: The front-end view template that displays the quiz interface.
- public/styles/main.css: Styles for the front-end.

## How to Use
- Access the app in your browser at http://localhost:3000.
- A flag will be displayed; enter the country name in the text box and submit.
- The score will increase with each correct answer. If you answer incorrectly, you can restart the game.

## Dependencies
- Express: For setting up the server and routing.
- Body-parser: Middleware to parse incoming request bodies.
- pg: PostgreSQL client for Node.js.
- dotenv: For loading environment variables.
