
# SCI-short - URL Shortener App

SCI-short is a URL shortener application built with Flask-RestX and React. It allows users to shorten long URLs into shorter, more manageable links.

## Features

- Shorten long URLs to short, custom links
- Redirect users to the original long URLs when they access the shortened links
- Track and analyze click statistics for each shortened link
- User registration and authentication
- User dashboard to manage and view their shortened links

## Technologies Used

- Frontend:
  - React: JavaScript library for building user interfaces
  - React Router: Routing library for React applications
  - Bootstrap: CSS framework for responsive and modern UI design

- Backend:
  - Flask: Python web framework for building the RESTful API
  - Flask-RestX: Extension for building REST APIs with Flask
  - SQLAlchemy: Python SQL toolkit and Object-Relational Mapping (ORM) library
  - PostgreSQL: Relational database management system for data persistence
  - PyJWT: JSON Web Token implementation for user authentication
 
## Live Pages
  - [Hosted Backend](https://sci-short-api.onrender.com/)
  - [Hosted Frontend](https://sci-short.onrender.com)

## Getting Started

These instructions will help you get a local development copy of the SCI-short app up and running.

### Prerequisites

- Node.js: Ensure that you have Node.js installed on your machine.
- Python: Make sure you have Python installed, preferably version 3.x.

### Installation and Setup

1. Clone the repository:
   ```
   git clone https://github.com/temitope3201/Sci-Short.git
   cd Sci-Short
   ```

2. Set up the backend:
   - Create a virtual environment (recommended) and activate it.
   - Install the required Python packages:
     ```
     pip install -r requirements.txt
     ```
   - Configure the database connection in the `backend/config.py` file.
   - Create A `.env` file in the root directory with the following variables.
        ```
          SECRET_KEY = 'your secret key'
          JWT_SECRET_KEY = 'your JWT secret key'
          DEBUG = TRUE
          IMGUR_CLIENT_ID = "client id for an imgur account"
          IMGUR_CLIENT_SECRET = "client secret for an imgur account"
        ```
   - In the terminal run
       ```
         set FLASK_APP=api/
       ```
       ```
         flask run
       ```
       ```
         db.create_all()
       ```
   - Apply the database migrations:
     ```
     flask db upgrade
     ```
   - Start the Flask-RestX backend server:
     ```
     python runserver.py
     ```

2. Set up the frontend:
   - Navigate to the `myapp` directory:
     ```
     cd frontend
     ```
   - Install the dependencies:
     ```
     npm install
     ```
   - Start the React development server:
     ```
     npm start
     ```

3. Access the application:
   - Open your web browser and go to `http://localhost:3000` to access the SCI-short app.

## Usage

- Register a new user account or log in with existing credentials.
- Create a shortened link by entering a long URL and an optional custom slug.
- Access the shortened link, and you will be redirected to the original long URL.
- View your shortened links and click statistics in the user dashboard.

## Deployment

To deploy SCI-short to a production environment, you can follow these general steps:
- Set up a production server with necessary dependencies (Python, Node.js, PostgreSQL).
- Configure the production database connection in the `backend/config.py` file.
- Build the frontend for production:
  ```
  cd frontend
  npm run build
  ```
- Set up a web server (e.g., render) to serve the backend API and frontend build.
- Configure the necessary environment variables and settings for the production server.
- Start the backend server and configure it to run continuously (e.g., using Gunicorn).

Please refer to the official documentation of Flask, React, and your hosting provider for more detailed deployment instructions.

## Contributing

Contributions are welcome! If you'd like to contribute

to SCI-short, please follow these guidelines:

- Fork the repository.
- Create a new branch for your feature or bug fix.
- Make your changes and ensure they adhere to the project's coding style and guidelines.
- Write tests to cover your changes, if applicable.
- Commit your changes and push them to your forked repository.
- Submit a pull request with a detailed description of your changes.

## License

This project is licensed under the MIT License. See the [MIT LICENSE](LICENSE) file for details.

## Acknowledgments

- [Flask](https://flask.palletsprojects.com/)
- [Flask-RestX](https://flask-restx.readthedocs.io/)
- [React](https://reactjs.org/)
- [React Router](https://reactrouter.com/)
- [Bootstrap](https://getbootstrap.com/)

## Contact

If you have any questions or feedback regarding SCI-short, feel free to contact me at `temitopeadebayo749@gmail.com`.

Enjoy using SCI-short and happy URL shortening!
