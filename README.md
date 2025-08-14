# Nfc_demo

Hi! This is the official repository for the NFC Demo project. This project demonstrates the use of Near Field Communication (NFC) with Django for managing donations and volunteers, with a focus on authentication and real-world workflows. All code is structured for clarity, modularity, and ease of understanding, so you can learn and extend it for your own purposes.

---

## Project Overview

This repository contains a Django web application that integrates NFC technology into a donations and volunteer management system. The project is organized primarily under the `old_project` directory, which includes several Django apps:

- **auth_app**: Handles user authentication and profile management.
- **donation**: Manages donation records, donors, and donation processing.
- **volunteer_app**: Coordinates volunteer registration, attendance (potentially via NFC), and task assignments.

The application is suitable for NGOs, charities, and organizations looking to streamline their operations using NFC for secure, efficient data collection and management.

---

## Directory Structure

```
old_project/
├── auth_app/           # Authentication logic, user models, login/signup
├── donation/           # Donation models, views, and templates
├── volunteer_app/      # Volunteer management and NFC attendance
├── db.sqlite3          # SQLite database (for local development)
├── manage.py           # Django project management script
└── old_project/        # Django settings, URLs, and WSGI/ASGI setup
```

Each app follows Django best practices, with dedicated folders for models, views, templates, and admin customization.

---

## Key Features

- **NFC Integration**: Demo-ready structure for connecting with NFC readers to register attendance, log donations, or verify users.
- **User Roles**: Supports multiple user types (admins, volunteers, donors) with appropriate permissions.
- **Donation Tracking**: Log donations, generate reports, and manage donor lists.
- **Volunteer Management**: Register, schedule, and track volunteer participation.
- **Authentication**: Secure login and registration via Django’s built-in auth system.
- **Admin Dashboard**: Easily manage users, donations, and volunteers through Django admin.
- **Extensible**: Modular codebase for adding more apps or integrating different hardware.

---

## Getting Started

### Prerequisites

- Python 3.8+
- pip
- Django (see `requirements.txt` if available)
- NFC device/reader for full functionality (optional for demo)

### Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/sohailshk/Nfc_demo.git
   cd Nfc_demo/old_project
   ```

2. **Create and activate a virtual environment:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
   *(If `requirements.txt` is missing, manually install Django: `pip install django`)*

4. **Apply migrations:**
   ```bash
   python manage.py migrate
   ```

5. **Create a superuser:**
   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server:**
   ```bash
   python manage.py runserver
   ```

7. Open [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your browser to use the application.

---

## How NFC Works Here

- **Attendance**: Volunteers or donors can tap their NFC card on a reader. The system will automatically detect, authenticate, and log their participation.
- **Security**: NFC usage is secured via Django's authentication system and can be extended for role-based access.
- **Extending**: You can connect a USB, serial, or phone-based NFC reader and use Python libraries (like `nfcpy`) to interface with the backend.

---

## Customization

- **Templates**: All HTML templates can be found in each app’s `templates` directory. Customize them to match your organization’s branding.
- **Settings**: Edit `old_project/settings.py` to configure email, database, or third-party services.
- **Models**: Extend models in each app to add more fields or relationships.

---

## Database

- **Development**: Uses SQLite (`db.sqlite3`) for easy local setup.
- **Production**: Change the `DATABASES` setting in `settings.py` to use PostgreSQL, MySQL, etc.

---

## Contributing

1. Fork this repo.
2. Make your changes in a feature branch.
3. Push to your fork and submit a pull request.
4. Please include test cases and update documentation as needed.

---

## License

This project is currently unlicensed. Please contact the repository owner if you wish to use it for commercial purposes or need a license clarification.

---

## Author

- Sohail Sheikh ([sohailshk](https://github.com/sohailshk))

---

If you have any questions, feel free to open an issue or contact me directly!
