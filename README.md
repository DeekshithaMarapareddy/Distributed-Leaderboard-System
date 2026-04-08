# Distributed Leaderboard System

A lightweight real-time leaderboard built using TCP sockets.
The server stores scores in `leaderboard.json` and pushes live updates to all connected clients.

---

##  Requirements

* Python 3.10+
* Uses `tkinter` (included in the standard library)
* No external dependencies required

---

##  How to Run

### 1. Start the Server (run once)

```bash
python server.py
```

### 2. Start Clients

```bash
python client.py
```

For clients on different machines, update this in `client.py`:

```python
SERVER_HOST = "127.0.0.1"  # Replace with the server's IP address
```

---

##  Features

###  Score Submission

* Enter a team name and score
* Press **SUBMIT** (or Enter)
* Only the highest score per team is stored

###  Real-Time Updates

* All clients receive instant updates
* No manual refresh required

###  Persistence

* Data is stored in `leaderboard.json`
* Server retains data after restart

---

##  Project Structure

```
server.py          # TCP server (handles clients, storage, broadcasting)
client.py          # tkinter-based GUI client
leaderboard.json   # Auto-created file storing scores
```

---

##  How It Works

* Server handles multiple clients using sockets and threading
* Maintains leaderboard data in JSON format
* Broadcasts updates to all connected clients in real time
* Ensures only the highest score per team is preserved

---

##  Notes

* Run the server before starting clients
* Ensure firewall/network settings allow socket connections for multi-device use
