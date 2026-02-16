# OIBSIP_python_task_3
⚙️ How It Works
🔹 Server (server.py)

Creates a TCP socket

Binds to 127.0.0.1:5000

Listens for incoming connections

Requests username from client

Stores:

Connected clients

Usernames

Broadcasts:

Messages

Join notifications

Leave notifications

Uses threading to handle multiple clients simultaneously

🔹 Client (client.py)

Connects to server

Sends chosen username

Runs two threads:

receive() → Listens for messages

write() → Sends messages

Allows real-time chatting

🛠️ Technologies Used

Python 3.x

socket module (TCP networking)

threading module (concurrency)

▶️ Installation & Setup
1️⃣ Clone the Repository
git clone https://github.com/your-username/socket-chat-app.git
cd socket-chat-app

2️⃣ Run the Server
python server.py


You should see:

Server started. Waiting for connections...

3️⃣ Run the Client (in new terminals)

Open multiple terminals and run:

python client.py


Enter a username when prompted.

💻 Example Chat Session

Terminal 1 (Server)

Server started. Waiting for connections...
Connected with ('127.0.0.1', 52341)
Username is Keshav


Terminal 2 (Client 1)

Choose a username: Keshav
Connected to server!
Keshav joined the chat!


Terminal 3 (Client 2)

Choose a username: Rahul
Rahul joined the chat!


Now both users can send and receive messages in real time.

🧩 Code Flow
Server Flow
receive()
 ├── accept connection
 ├── request username
 ├── add to clients list
 ├── broadcast join message
 └── start handle_client() thread

Client Flow
main
 ├── connect to server
 ├── start receive thread
 └── start write thread

🔐 Networking Details

Protocol: TCP

IP Address: 127.0.0.1 (Localhost)

Port: 5000

Encoding: UTF-8

🚧 Limitations

Works only on localhost by default

No encryption (not secure for public deployment)

No GUI interface

No authentication system

🔮 Future Improvements

🌐 Deploy over LAN / Internet

🔐 Add encryption (SSL/TLS)

🖥️ Add GUI (Tkinter / PyQt)

👥 Private messaging feature

🗂️ Chat history saving

🛡️ Add authentication system

🎨 Color-coded usernames

🎓 Learning Concepts Covered

Client-Server Architecture

TCP Socket Programming

Multi-threading

Broadcast communication

Exception handling

🤝 Contributing

Pull requests are welcome.
For major changes, open an issue first to discuss improvements.

📜 License

This project is licensed under the MIT License.

👨‍💻 Author

Keshav Marda
