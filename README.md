# Sentiment Analysis Project

## 📝 Short Description

This is a complete sentiment analysis web application that uses Django backend and React frontend. Users can enter text and analyze its sentiment (positive, negative, neutral). The project includes user authentication, history tracking, and admin panel features. Sentiment analysis is performed using NLTK and TextBlob libraries. The UI is designed with modern Tailwind CSS.

## 🚀 Features

- **User Authentication** - Login and Signup system
- **Sentiment Analysis** - Analyzes text sentiment
- **History Tracking** - Records of previous analyses
- **Admin Panel** - Special permissions for admin users
- **Modern UI** - Beautiful interface with Tailwind CSS

## 📋 Prerequisites

Your system should have these installed:

- **Python 3.8+**
- **Node.js 14+**
- **npm** or **yarn**

## 🛠️ Installation

### Backend Setup

1. **Go to backend directory:**
```bash
cd backend
```

2. **Create virtual environment:**
```bash
python -m venv venv
```

3. **Activate virtual environment:**
```bash
# For Windows:
venv\Scripts\activate

# For Linux/Mac:
source venv/bin/activate
```

4. **Install dependencies:**
```bash
pip install -r requirements.txt
```

5. **Run database migrations:**
```bash
python manage.py migrate
```

6. **Create superuser (optional):**
```bash
python manage.py createsuperuser
```

7. **Start backend server:**
```bash
python manage.py runserver
```

Backend will be running on `http://localhost:8000`.

### Frontend Setup

1. **Go to frontend directory:**
```bash
cd sentiment-frontend
```

2. **Install dependencies:**
```bash
npm install
```

3. **Start frontend server:**
```bash
npm start
```

Frontend will be running on `http://localhost:3000`.

## 🎯 How to Use

1. **Go to `http://localhost:3000` in your browser**
2. **Sign up** or **login**
3. **Enter text** that you want to analyze
4. **Click "Analyze Sentiment" button**
5. **View results** - sentiment and polarity score

## 📁 Project Structure

```
sentiment_project/
├── backend/
│   ├── sentiment_app/          # Main sentiment analysis app
│   ├── users/                  # User authentication app
│   ├── sentiment_project/      # Django settings
│   ├── requirements.txt        # Python dependencies
│   └── manage.py              # Django management
├── sentiment-frontend/
│   ├── src/
│   │   ├── App.js             # Main React component
│   │   └── ...
│   ├── package.json           # Node.js dependencies
│   └── ...
└── README.md                  # This file
```

## 🔧 API Endpoints

- `POST /api/auth/login/` - User login
- `POST /api/auth/signup/` - User registration
- `POST /api/sentiment/analyze/` - Sentiment analysis
- `GET /api/sentiment/history/` - Analysis history
- `DELETE /api/sentiment/delete/{id}/` - Delete analysis (admin only)

## 🛡️ Security Features

- **JWT Authentication** - Secure token-based auth
- **CORS Configuration** - Cross-origin requests
- **Input Validation** - Server-side validation
- **Admin Permissions** - Role-based access control

## 🎨 Technologies Used

### Backend
- **Django 5.2.4** - Web framework
- **Django REST Framework** - API development
- **NLTK** - Natural Language Processing
- **TextBlob** - Sentiment Analysis
- **SQLite** - Database (development)

### Frontend
- **React 19.1.1** - UI framework
- **Tailwind CSS** - Styling
- **Lucide React** - Icons
- **JWT** - Authentication

## 🐛 Troubleshooting

### Common Issues:

1. **Port already in use:**
   - Backend: `python manage.py runserver 8001`
   - Frontend: `PORT=3001 npm start`

2. **Dependencies not installing:**
   - `pip install --upgrade pip`
   - `npm cache clean --force`

3. **Database errors:**
   - `python manage.py makemigrations`
   - `python manage.py migrate`

## 📝 Environment Variables

Create a `.env` file in backend:

```env
SECRET_KEY=your-secret-key-here
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
```

## 🚀 Deployment

### Production Setup:

1. **Database**: Use PostgreSQL instead of SQLite
2. **Static Files**: `python manage.py collectstatic`
3. **Environment**: Set `DEBUG=False`
4. **HTTPS**: Configure SSL certificate

## 📞 Support

If you encounter any issues:
- Check that all dependencies are installed
- Check console errors
- Verify network connectivity

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Submit a pull request

---

**Happy Coding! 🎉** 