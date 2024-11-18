Flask Web Application

This is a Flask-based web application designed to handle form submissions and save the collected data into a text file (database.txt) or a CSV file (database.csv). The application also serves dynamic HTML pages.

- Features

Serves HTML files dynamically.
Processes form submissions using Flask's request handling.
Stores submitted data in a text file and a CSV file.
Includes basic error handling during data storage.

File Overview

1. app.py
   
- Flask Setup: Initializes the Flask app with Flask(__name__).

- Routes:
"/": Renders the index.html homepage.
"/<string:page_name>": Dynamically serves other HTML pages based on the route.
"/submit_form": Handles form submissions, processes the data, and saves it to a text or CSV file.

- Utility Functions:
  
write_to_file(data): Appends form data to database.txt.
write_to_csv(data): Appends form data to database.csv.

2. templates/index.html
The homepage of the application. This is served via the root ("/") route.

3. templates/thankyou.html
Displays a thank-you message after successful form submission.

4. database.txt
Stores submitted form data in plain text format.

5. database.csv
Stores submitted form data in CSV format

- Application Flow

1. User accesses the root route ("/"), which serves the index.html page.
2. When the user submits a form, the data is sent to the "/submit_form" route.
3. Data is processed:
  - If successful, it is saved to both database.txt and database.csv.
  - The user is redirected to the thankyou.html page.
  - If an error occurs, a message is displayed indicating the failure.

- Prerequisites

Python 3.x installed.
Flask installed (pip install flask).
Basic understanding of Flask and web development.

- Contributing

Feel free to fork the repository, make changes, and create pull requests to contribute!

