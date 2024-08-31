# Platformer Game with High Score Tracking

This project is a 2D platformer game developed in C# using Visual Studio. The game features a high score tracking system that uses phpMyAdmin to store and retrieve scores. When a player achieves a new high score, the system automatically updates the stored high score in the database.

## Features
- **2D Platformer Gameplay:** Classic platformer mechanics including running, jumping, and avoiding obstacles.
- **High Score Tracking:** The game records and displays the highest score achieved by players.
- **Database Integration:** Scores are stored in a MySQL database managed through phpMyAdmin.
- **Automatic High Score Updates:** If a player beats the current high score, the database is automatically updated.

## Requirements
- **Visual Studio:** Development environment used to write and debug the game code.
- **C# Programming Language:** The game is developed using C#.
- **MySQL Database:** Used for storing high scores.
- **phpMyAdmin:** Tool for managing the MySQL database.

## Setup Instructions

### 1. Database Setup
1. Install MySQL and phpMyAdmin on your local machine or server.
2. Create a new database named `PlatformerGame`.
3. Create a table named `HighScores` with the following structure:

    - `id`: INT, Auto Increment, Primary Key
    - `player_name`: VARCHAR(50), Not Null
    - `score`: INT, Not Null
    - `achieved_at`: TIMESTAMP, Default to Current Timestamp

4. Insert an initial high score to start the tracking.

### 2. Visual Studio Setup
1. Clone the repository or download the project files.
2. Open the solution in Visual Studio.
3. Ensure the necessary NuGet packages are installed for MySQL database connectivity:
    - MySql.Data

4. Configure the connection string in the `App.config` file to connect to your MySQL database.

### 3. High Score Logic
- The game retrieves the current high score from the database when it starts.
- After each game session, the player's score is compared to the high score.
- If the player's score exceeds the high score, the database is updated with the new high score.

### 4. Running the Game
1. Build the solution in Visual Studio.
2. Run the game and enjoy!

## Contributing
Contributions are welcome! Please fork this repository and submit a pull request for any features, bug fixes, or improvements.
