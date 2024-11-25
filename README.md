# Youth Creativity and Expression Hub
The Youth Creativity and Expression Hub is a digital platform designed to empower young individuals by providing a space to explore, showcase, and develop their creative talents. Users can share their work and connect with mentors.

## Features
### Core Functionalities
- **User Profiles:**
Create personalized profiles with bio, areas of interest, and role (e.g., user or mentor).

- **Content Sharing:**
Upload and showcase creative works in categories like art, music, writing, and more.

- **Mentorship:**
Connect with mentors, schedule mentorship sessions, and receive guidance on creative projects.

- **Direct Messaging:**
Communicate with peers and mentors through a secure messaging system.

## Installation
### Prerequisites
Ensure the following are installed on your system:

- **Python 3.8+**
- **MYSQL Server**
- **A virtual environment manager**

Python dependencies (included in requirements.txt):

authlib ~= 1.2
django ~= 4.2
python-dotenv ~= 1.0
requests ~= 2.31
daphne ~= 4.1 

### Setup Instructions
1. Clone the Repository:

```sh
git clone https://github.com/NadiaTeta/YouthTalent.git
cd YouthTalent
```

2. Create a Virtual Environment:

```sh
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

3. Install Dependencies:

```sh
pip install -r requirements.txt
```
4. Start MYSQL Server

```sh
sudo systemctl start mysql
sudo mysql -u root -p
```
5. Create a Database
After logging into MYSQL:
   
```sh
CREATE DATABASE youthcreativity;
exit;
```
6. Update Database Settings
Open settings.py in your Django project and update the DATABASES configuration:

```sh
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'youthcreativity',
        'USER': 'your_mysql_user',
        'PASSWORD': 'your_mysql_password',
        'HOST': 'localhost',
    }
}
```

7. Run Database Migration

```sh
python manage.py makemigrations
python manage.py migrate
```

8. Run the Development Server:

```
python manage.py runserver
```

9. Access the Application:
Open your browser and navigate to http://localhost:8000.

## Folder Structure
```sh
├── assets/        # Contains additional assets like fonts or external libraries.
├── chat/          # Django app for chat functionality.
├── core/          # Django app for core functionalities (e.g., posts, events).
├── media/         # Stores user-uploaded files (e.g., profile pictures, creative works).
├── static/        # Stores static files like CSS, JavaScript, and images.
├── templates/     # Contains HTML templates for the Django views.
├── users/         # Django app for user authentication and profiles.
├── .env           # Environment variables (e.g., database credentials).
├── README.md      # Project documentation.
├── db.sqlite3     # SQLite database file (used for development/testing).
├── manage.py      # Django’s command-line utility for administrative tasks.
├── requirements.txt  # List of project dependencies.
└── response.json())
```
- **core/: Handles posts, events, and collaboration tools.**
- **users/: Manages user registration, authentication, and profiles.**
- **chat/: Implements direct messaging and mentorship chat functionalities.**
- **templates/: HTML templates for views.**
- **static/: Static assets like CSS, JS, and images.**
- **media/: User-uploaded files (e.g., profile pictures, creative works).**
   
## Technologies Used
1. Backend: Django (Python)
2. Frontend: HTML, CSS, JavaScript
3. Database: MySql
4. Websocket Server: Daphne ~4.1 (for handling WebSockets)
   
## Contributing
We welcome contributions! Follow these steps to contribute:

1. Fork the repository.
2. Create a feature branch:
```sh
   git checkout -b feature-name
```
3. Commit changes:
```sh
   git commit -m "Add feature"
```
4. Push to your branch:
```sh
   git push origin feature-name
```
5. Submit a pull request.
 
## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Contact
For queries or suggestions, please reach out to:
Email: support@youthcreativityhub.com
GitHub: YouthTalent
