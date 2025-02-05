# 🎵 Spotify-Like App

## 📌 Overview
This is a **Spotify-like music streaming app** built with **React (frontend)** and **Django (backend)**. The project allows users to create and join rooms, control music playback, and interact with the system using Spotify's API.

## 🚀 Tech Stack
### Frontend:
- React.js
- React Router
- Material UI / Tailwind CSS (optional for styling)
- Sqlite

### Backend:
- Python & Django
- Django REST Framework (DRF)
- Spotify Web API
- SQLite (for database management)

## 🔧 Features
### 🎶 Music Streaming
- Users can **connect their Spotify account**
- Control **playback (play, pause, skip)**
- View **currently playing song**

### 🏠 Room Management
- Create **music rooms** with a unique code
- Join existing rooms
- Vote to skip songs
- Automatic room deletion if host leaves

## ⚙️ Installation Guide
### 📌 Backend (Django API)
1. **Clone the repository**
   ```sh
   git clone https://github.com/mehdidinari/spotify-app.git
   cd spotify-app/backend
   ```
2. **Create a virtual environment**
   ```sh
   python -m venv env
   source env/bin/activate  # On Windows use: env\Scripts\activate
   ```
3. **Install dependencies**
   ```sh
   pip install -r requirements.txt
   ```
4. **Set up environment variables**
   - Create a `.env` file and add your **Spotify API credentials**:
     ```env
     SPOTIFY_CLIENT_ID=your_client_id
     SPOTIFY_CLIENT_SECRET=your_client_secret
     SPOTIFY_REDIRECT_URI=http://localhost:8000/spotify/redirect
     ```
5. **Run migrations and start server**
   ```sh
   python manage.py migrate
   python manage.py runserver
   ```

### 🎨 Frontend (React)
1. **Navigate to frontend directory**
   ```sh
   cd ../frontend
   ```
2. **Install dependencies**
   ```sh
   npm install
   ```
3. **Start the React app**
   ```sh
   npm start
   ```

## 🔗 API Endpoints
| Method | Endpoint | Description |
|--------|---------|-------------|
| GET | `/api/spotify/auth-url/` | Get Spotify authentication URL |
| POST | `/api/spotify/is-authenticated/` | Check if user is authenticated |
| POST | `/api/spotify/play/` | Play the current track |
| POST | `/api/spotify/pause/` | Pause playback |
| GET | `/api/spotify/current-song/` | Get currently playing song |
| POST | `/api/room/create/` | Create a new room |
| GET | `/api/room/<room_code>/` | Get room details |

## 🎯 Roadmap
- ✅ Basic Spotify API integration
- ✅ User authentication with Spotify
- ✅ Room creation & joining
- ⏳ Live chat feature (Upcoming)
- ⏳ Playlist creation and management
- ⏳ Mobile responsive design

## 🤝 Contributing
Pull requests are welcome! To contribute:
1. Fork the repository
2. Create a new feature branch (`git checkout -b feature-name`)
3. Commit your changes (`git commit -m 'Add new feature'`)
4. Push to the branch (`git push origin feature-name`)
5. Submit a pull request

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
💡 **Made with ❤️ by [Mehdi Dinari](https://github.com/mehdidinari)**

