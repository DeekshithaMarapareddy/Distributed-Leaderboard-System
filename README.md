**# distributed-leaderboard-system**
A lightweight real-time leaderboard built using TCP sockets.
The server stores scores in leaderboard.json and instantly pushes updates to all connected clients.

**Requirements**
Python 3.10+
Uses tkinter (included in the standard library)
No external dependencies required
**How to Run**
1. Start the Server (run once on any machine)
python server.py
2. Start Clients (run on same or different machines)
python client.py

For clients on different machines, update this in client.py:

SERVER_HOST = "127.0.0.1"  # Replace with the server's IP address
**Features**
Score Submission
Enter a team name and score, then press SUBMIT (or hit Enter).
Only the highest score per team is recorded.
Real-Time Updates
All connected clients receive instant updates whenever scores change.
No need to refresh manually.
Data Persistence
Scores are saved in leaderboard.json, allowing the server to retain data even after restarts.
**Project Structure**
server.py          # Handles connections, data storage, and broadcasting updates  
client.py          # GUI client built with tkinter  
leaderboard.json   # Auto-generated file storing scores  
