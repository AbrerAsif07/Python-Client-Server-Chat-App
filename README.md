Python Client-Server Chat Application

A GUI-based chat application built in Python using socket, threading, and customtkinter. This project allows multiple users to connect to a central server and exchange messages and images in real-time.

📦 Features:
- 👤 Signup/Login system (simple local check)  
- 💬 Real-time messaging using sockets
- 🖼️ Send images in chat
- 🧑‍💻 Multi-client support
- 🪟 User-friendly GUI with customtkinter
- 🌐 Works on a single PC or across multiple devices on the same network

## Libraries Used:

This project utilizes the following Python libraries:

| Library           | Purpose                                                    |
|-------------------|------------------------------------------------------------|
| `socket`          | Enables network communication between client and server.   |
| `threading`       | Allows handling send/receive operations concurrently.     |
| `os`, `sys`       | Provides file operations and system access.              |
| `customtkinter`   | Offers a modern themed GUI for Python desktop applications.|
| `tkinter.filedialog`| Provides a file selection dialog for sending images.      |
| `PIL` (Pillow)    | Opens and resizes images for display in the chat.        |
| `datetime`        | Generates timestamps for messages.   

Install missing packages using:
pip install customtkinter pillow

🔄 Application Flow

1. Server Side (server.py)  
- Starts listening on a specified IP and port.  
- Accepts client connections using threading for each.  
- Receives messages or files and broadcasts to all connected clients.  
- Logs chat history and handles authentication requests.

2. Client Side (Client.py)
- Launches a GUI window for Login or Sign Up.  
- Sends mode (Login / Register) to the server.  
- Exchanges credentials (USERNAME, PASSWORD, EMAIL) with the server.  
- On success, opens the Chat Window:  
- Displays chat in a ScrolledText widget.  
- Allows sending text messages and selecting images to send.  
- Handles incoming messages/files in a background thread.  

# How to Run (Option A: Single PC)

1.Clone the repository:  
git clone https://github.com/YourUsername/Python-Client-Server-Chat-App.git  
cd Python-Client-Server-Chat-App  

2.Install dependencies:  
pip install customtkinter pillow  

3.Start the server:  
python server.py  

4.Start Client #1 in a new terminal:  
python Client.py  

5.Start Client #2 in another terminal to simulate a second user:  
python Client.py  


# 🌍 How to Run (Option B: Multiple PCs on Same Wi-Fi)

- 1.Find the host PC's local IP on Windows: ipconfig
- HOST = '192.168.1.5'  # replace with your server's IP
- 2.Allow Python through the firewall on the host if prompted.
- Run the server on the host machine:  python server.py
- 3.On each client machine (same Wi-Fi):
- Clone the repo or copy the folder
- Update HOST as above
- Run: python Client.py
- 4.Start chatting between devices!

- 🙌 Contributing

- Feel free to fork this repository, create a feature branch, and issue a pull request. All suggestions and improvements are welcome
---
