# 💬 Real-Time Chat Application

A real-time messaging web application built using **Django Channels**, **WebSockets**, **Redis**, and **PostgreSQL**. The application enables instant communication with private messaging, group chats, online/offline status tracking, and persistent chat history.

---

## 🚀 Features

- 🔐 User Authentication (Sign Up / Login / Logout)
- 💬 One-to-One Private Messaging
- 👥 Group Chat Support
- ⚡ Real-Time Messaging using WebSockets
- 🟢 Online / Offline User Status
- 📜 Persistent Chat History
- 👤 User Profiles
- 📱 Responsive User Interface
- 🔄 Instant Message Updates
- 🗄 PostgreSQL Database Integration
- ⚙️ Asynchronous Communication with Django Channels
- 🚀 Redis Channel Layer for High Performance

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|----------|
| Python | Backend Programming |
| Django | Web Framework |
| Django Channels | Real-Time Communication |
| WebSocket | Bi-Directional Messaging |
| Redis | Channel Layer |
| PostgreSQL | Database |
| HTML5 | Frontend Structure |
| CSS3 | Styling |
| JavaScript | Client-Side Logic |
| Bootstrap | Responsive Design |

---

## 📂 Project Structure

```
realtime-chat/
│
├── chat/
│   ├── consumers.py
│   ├── routing.py
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   └── templates/
│
├── users/
│
├── static/
│
├── media/
│
├── realtime_chat/
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
├── requirements.txt
├── manage.py
└── README.md
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/realtime-chat.git

cd realtime-chat
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

### 3. Activate the Virtual Environment

**Windows**

```bash
venv\Scripts\activate
```

**Linux / macOS**

```bash
source venv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🗄 Configure PostgreSQL

Create a PostgreSQL database and update the database settings in **settings.py**.

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'chat_db',
        'USER': 'postgres',
        'PASSWORD': 'password',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

---

## 🚀 Configure Redis

Install Redis

### Ubuntu

```bash
sudo apt install redis-server
```

Start Redis

```bash
redis-server
```

Verify Installation

```bash
redis-cli ping
```

Output

```
PONG
```

---

## ▶️ Run the Project

Apply migrations

```bash
python manage.py makemigrations

python manage.py migrate
```

Create an admin account

```bash
python manage.py createsuperuser
```

Start the development server

```bash
python manage.py runserver
```

Visit

```
http://127.0.0.1:8000/
```

---

## 🌐 WebSocket Routing Example

```python
from django.urls import re_path
from .consumers import ChatConsumer

websocket_urlpatterns = [
    re_path(r'ws/chat/(?P<room_name>\w+)/$', ChatConsumer.as_asgi()),
]
```

---

## ⚡ Performance Optimizations

- Implemented asynchronous WebSocket consumers using Django Channels
- Used Redis as the Channel Layer
- Optimized database queries with `select_related()` and `prefetch_related()`
- Persistent PostgreSQL storage for chat history
- Designed to support **200+ concurrent WebSocket connections**
- Low-latency message delivery with minimal data loss

---

## 📸 Screenshots

You can add screenshots here.

```
screenshots/
├── login.png
├── register.png
├── private-chat.png
├── group-chat.png
└── profile.png
```

---

## 🔮 Future Enhancements

- 📁 File Sharing
- 😊 Emoji Support
- 🎤 Voice Messages
- 📹 Video Calling
- ✔️ Read Receipts
- ❤️ Message Reactions
- 🔔 Push Notifications
- 🔒 End-to-End Encryption
- 🌙 Dark Mode

---

## 📌 Resume Highlights

- Developed a scalable real-time chat application using Django Channels, WebSockets, Redis, and PostgreSQL.
- Implemented private messaging, group chats, online/offline status, and persistent message history.
- Built asynchronous WebSocket consumers for efficient real-time communication.
- Optimized PostgreSQL queries using `select_related()` and `prefetch_related()`.
- Designed the backend to efficiently handle **200+ concurrent WebSocket connections**.

---

## 👨‍💻 Author

**Rishi Mishra**

📧 **Email:** getrishimishra@gmail.com

🐙 **GitHub:** https://github.com/getrishimishra

💼 **LinkedIn:** https://linkedin.com/in/Rishimishraa

---

## ⭐ Show Your Support

If you found this project useful, consider giving it a ⭐ on GitHub.

---

## 📄 License

This project is licensed under the **MIT License**.
