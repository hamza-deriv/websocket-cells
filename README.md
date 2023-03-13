# Websocket Cells
This is a simple web-based game built with HTML, JavaScript, and WebSocket API. The game allows users to create and join games, where players can click on a ball to change its color. The game is built to be played in real-time with multiple players.

## Installation
Install the required dependencies by running `npm i`

## Getting Started
To run the game, simply run `node index.js`

## Usage
- Click on the "New Game" button to create a new game.
- Click on the "Join Game" button to join an existing game by entering its ID.
- Once you have joined a game, you will see a list of players and a board with numbered balls.
- Click on a ball to change its color to your player's color.
- The game will update in real-time to show the colors of all players.

## WebSocket API
The game uses the WebSocket API to establish a real-time connection between the client and server. The client sends and receives JSON messages to communicate with the server. The following methods are available:

### `connect`
This method is used to establish a connection with the server. When a client connects to the server, the server assigns a unique clientId to the client and sends it back to the client in the response.

### `create`
This method is used to create a new game. When a client creates a new game, the server generates a unique gameId and sends it back to the client in the response.

### `join`
This method is used to join an existing game. When a client joins a game, the server sends back the current state of the game, including the list of players and the color of each ball.

### `play`
This method is used to change the color of a ball. When a player clicks on a ball, the client sends a play message to the server with the clientId, gameId, ballId, and color of the player. The server updates the state of the game and sends an update message to all players to update the color of the ball.

## Contributing
If you find any bugs or issues with the game, feel free to submit a pull request or open an issue on GitHub.
