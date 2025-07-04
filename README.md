# 🚗 Car Dealership Management System

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.12-blue.svg)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-5.0-green.svg)](https://www.djangoproject.com/)
[![React](https://img.shields.io/badge/React-18.2-blue.svg)](https://reactjs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-6.3-green.svg)](https://www.mongodb.com/)
[![Node.js](https://img.shields.io/badge/Node.js-18+-green.svg)](https://nodejs.org/)

A comprehensive full-stack web application for managing car dealerships, built with modern technologies including Django REST Framework, React, and MongoDB. This system allows users to browse dealerships, view car inventory, post reviews, and manage customer interactions.

## ✨ Features

### 🏪 Dealership Management
- Browse and search car dealerships nationwide
- View detailed dealership information including location, contact details, and services
- Interactive map integration for dealership locations

### 🚙 Car Inventory
- Comprehensive car catalog with makes, models, and specifications
- Filter cars by make, model, year, type, and price range
- Detailed car information with images and specifications

### 💬 Review System
- Customer review and rating system
- Sentiment analysis for review insights
- Review moderation and management tools

### 👤 User Management
- User registration and authentication
- Profile management
- Role-based access control

### 📊 Analytics Dashboard
- Sales analytics and reporting
- Customer insights and trends
- Inventory management reports

## 🏗️ Architecture

### Frontend
- **React 18.2** - Modern UI with hooks and functional components
- **React Router** - Client-side routing
- **Bootstrap** - Responsive design and styling
- **Axios** - API communication

### Backend
- **Django 5.0** - Web framework with REST API
- **Django REST Framework** - API development
- **Python 3.12** - Core programming language
- **Gunicorn** - WSGI HTTP Server

### Database
- **MongoDB** - Primary database for dealership and review data
- **SQLite** - Django's default database for user management
- **Mongoose** - MongoDB object modeling

### DevOps & Deployment
- **Docker** - Containerization
- **Kubernetes** - Container orchestration
- **GitHub Actions** - CI/CD pipeline

## 🚀 Quick Start

### Prerequisites
- Python 3.12+
- Node.js 18+
- MongoDB 6.3+
- Docker (optional)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/car-dealership-management.git
   cd car-dealership-management
   ```

2. **Setup Python Environment**
   ```bash
   cd server
   python -m venv djangoenv
   source djangoenv/bin/activate  # On Windows: djangoenv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Setup Database Services**
   ```bash
   cd database
   npm install
   node app.js
   ```

4. **Setup Django Backend**
   ```bash
   cd ../
   python manage.py migrate
   python manage.py populate  # Load initial data
   python manage.py runserver
   ```

5. **Setup React Frontend**
   ```bash
   cd frontend
   npm install
   npm start
   ```

### 🐳 Docker Deployment

1. **Build and run with Docker**
   ```bash
   docker build -t car-dealership .
   docker run -p 8000:8000 car-dealership
   ```

2. **Using Docker Compose**
   ```bash
   cd database
   docker-compose up -d
   ```

3. **Kubernetes Deployment**
   ```bash
   kubectl apply -f deployment.yaml
   ```

## 📁 Project Structure

```
├── server/
│   ├── djangoapp/           # Main Django application
│   │   ├── models.py        # Database models
│   │   ├── views.py         # API views
│   │   ├── urls.py          # URL routing
│   │   └── restapis.py      # External API integration
│   ├── djangoproj/          # Django project settings
│   ├── database/            # MongoDB microservice
│   │   ├── app.js           # Express server
│   │   ├── dealership.js    # Dealership API
│   │   ├── inventory.js     # Car inventory API
│   │   └── review.js        # Review system API
│   ├── frontend/            # React application
│   │   ├── src/
│   │   │   ├── components/  # React components
│   │   │   └── App.js       # Main App component
│   │   └── public/          # Static assets
│   └── static/              # Django static files
├── deployment.yaml          # Kubernetes deployment
├── dockerfile               # Docker configuration
└── requirements.txt         # Python dependencies
```

## 🛠️ API Endpoints

### Authentication
- `POST /api/login` - User login
- `POST /api/register` - User registration
- `GET /api/logout` - User logout

### Dealerships
- `GET /api/dealerships` - List all dealerships
- `GET /api/dealership/:id` - Get dealership details
- `GET /api/dealership/:id/reviews` - Get dealership reviews

### Cars
- `GET /api/cars` - List all cars
- `GET /api/cars/:id` - Get car details
- `GET /api/cars/search` - Search cars with filters

### Reviews
- `POST /api/reviews` - Submit a review
- `GET /api/reviews/:id` - Get review details
- `PUT /api/reviews/:id` - Update review
- `DELETE /api/reviews/:id` - Delete review

## 🧪 Testing

### Backend Tests
```bash
cd server
python manage.py test
```

### Frontend Tests
```bash
cd server/frontend
npm test
```

### API Testing
```bash
# Using curl
curl -X GET http://localhost:8000/api/dealerships

# Using Postman
Import the provided Postman collection
```

## 🔧 Configuration

### Environment Variables
Create a `.env` file in the server directory:
```env
DEBUG=True
SECRET_KEY=your-secret-key
DATABASE_URL=mongodb://localhost:27017/dealership
SENTIMENT_API_KEY=your-sentiment-api-key
```

### Database Configuration
- MongoDB connection string in `database/app.js`
- Django database settings in `djangoproj/settings.py`

## 📈 Performance Optimization

- **Caching**: Redis integration for API response caching
- **Database Indexing**: Optimized MongoDB queries
- **CDN**: Static asset delivery via CDN
- **Load Balancing**: Nginx reverse proxy configuration

## 🔐 Security Features

- JWT authentication
- CORS configuration
- Input validation and sanitization
- SQL injection prevention
- XSS protection

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📋 Roadmap

- [ ] Mobile application (React Native)
- [ ] Advanced analytics dashboard
- [ ] Integration with external automotive APIs
- [ ] Real-time chat support
- [ ] AI-powered car recommendations
- [ ] Blockchain-based vehicle history

## 🐛 Known Issues

- Review sentiment analysis requires API key configuration
- Mobile responsive design needs improvement
- Image upload functionality in development

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Team

- **Full Stack Developer** - Initial work and maintenance
- **UI/UX Designer** - Interface design and user experience
- **DevOps Engineer** - Deployment and infrastructure

## 📞 Support

For support, create an issue in the GitHub repository.

## 🙏 Acknowledgments

- IBM Full Stack Developer Capstone Project
- React community for excellent documentation
- Django REST Framework contributors
- MongoDB community and documentation

---

<p align="center">
  Made with ❤️ by Mohab
</p>
