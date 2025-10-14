# Mergington High School Activities

A comprehensive web application built with FastAPI that enables students to explore, filter, and sign up for extracurricular activities at Mergington High School. The application features a modern, responsive interface with advanced filtering capabilities and secure teacher authentication for student registration management.

## Features

### Core Functionality
- **Activity Browsing**: View all available extracurricular activities with detailed information including descriptions, schedules, and participant counts
- **Student Registration**: Teachers can sign up students for activities and unregister them as needed
- **Capacity Management**: Real-time tracking of available spots with visual indicators for capacity status

### Advanced Filtering & Search
- **Search**: Find activities by name or description using the search bar
- **Category Filtering**: Filter activities by type (Sports, Arts, Academic, Community, Technology)
- **Day Filtering**: View activities by specific days of the week (Monday through Sunday)
- **Time Filtering**: Filter by time periods (Before School, After School, Weekend)

### Authentication & Security
- **Teacher Authentication**: Secure login system for teachers to manage student registrations
- **Session Management**: Persistent login sessions with proper logout functionality
- **Role-based Access**: Authentication required for student registration and management

### User Interface
- **Responsive Design**: Modern, mobile-friendly interface that works on all devices
- **Interactive Elements**: Modal dialogs for registration and authentication
- **Visual Indicators**: Color-coded capacity status (Available, Near Full, Full)
- **Activity Cards**: Rich display of activity information with tags and scheduling details

## Technology Stack

- **Backend**: FastAPI (Python web framework)
- **Database**: MongoDB for data persistence
- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Server**: Uvicorn ASGI server
- **Authentication**: Session-based authentication with password hashing

## API Endpoints

The application provides a RESTful API with the following main endpoints:

### Activities
- `GET /activities` - Retrieve all activities with optional filtering by day and time
- `GET /activities/days` - Get list of days that have scheduled activities
- `POST /activities/{activity_name}/signup` - Register a student for an activity (requires teacher authentication)
- `POST /activities/{activity_name}/unregister` - Remove a student from an activity (requires teacher authentication)

### Authentication
- `POST /auth/login` - Teacher login with username and password
- `GET /auth/check-session` - Validate existing session

### Interactive API Documentation
- **Swagger UI**: Available at `/docs` when running the application
- **ReDoc**: Alternative documentation at `/redoc`

## Database

The application uses MongoDB to store:
- **Activities**: Complete activity information including schedules, descriptions, and participant lists
- **Teachers**: Authentication credentials and profile information
- **Sample Data**: Pre-populated with diverse activities across multiple categories and time slots

## Development Guide

For detailed setup and development instructions, including environment setup, debugging, and deployment, please refer to our comprehensive [Development Guide](../docs/how-to-develop.md).
