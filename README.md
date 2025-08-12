# Connect Four
- Create a **real-time multiplayer game server** using Node.js 
- Allow users to play 1v1 (vs player or bot)
- Build a simple **frontend UI** for interaction

# Demo Link :
https://drive.google.com/file/d/1LjKdBsuIG3Q5Ebb6ET4T3vzBYcnpWBN3/view?usp=drive_link
# Live Link :
https://frontendconnect.vercel.app/

 ## Game Rules – 4 in a Row

The game is played on a **7×6 grid**. Players take turns dropping discs into one of the columns. The disc falls to the lowest available space in that column.

## Requirements

### 1. 🧍 Player Matchmaking

- Players enter a username and wait for an opponent.
- If no second player joins within **10 seconds**, a **competitive bot** should start the game with the waiting user.

### 2. 🧠 Competitive Bot

- The bot must:
    - Play with valid game logic
    - Make **strategic decisions** to:
        - Block the opponent from winning
        - Try to win when it has an opportunity
    - Respond quickly to player moves
    
    ❗ The bot should **not** play random moves. It should analyse the board and prioritise:
    
    - Blocking player’s immediate win
    - Creating its own winning path###
    
### 3. 🌐 Real-Time Gameplay

- Use **WebSockets** to support real-time turn-based play.
- Both players should see updates immediately after each move.
- **If a player disconnects**, they should be able to **rejoin the same game within 30 seconds** using their username or game ID.
- If they don’t reconnect within 30 seconds:
    - The game is forfeited.
    - The opponent (or bot) is declared the winner.

### 4. 🧾 Game State Handling

- Maintain in-memory state for active games.
- Store completed games persistently (e.g. Postgres).

### 5. 🏅 Leaderboard

- Track **number of games won per player**.
- show leaderboard on the frontend.

### Winning Conditions:

- The first player to connect **4 discs** vertically, horizontally, or diagonally wins.
- If the board fills up with no winner, the game is a **draw**.

## Technologies Used

 Backend: Node.js, Express, WebSocket

 Frontend: React.js (or your frontend framework)

Others: UUID for unique IDs, dotenv for environment variables

Installation
Clone the repository:
```

git clone https://github.com/your-username/connect-four.git
cd connect-four
```
Install backend dependencies:
```

cd backend
npm install
```
Install frontend dependencies (if applicable):
```

cd ../frontend
npm install
```
Create a .env file in the backend folder (if needed) and configure environment variables like PORT.

Usage
Start the backend server:
```

npm start
```
Start the frontend app:
```
npm start
```
Open your browser at http://localhost:3000 (or your frontend port) to play the game.
