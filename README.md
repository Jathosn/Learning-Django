To run this project locally you need to set up a MySQL server. Download the most recent installer from https://dev.mysql.com/downloads/installer/ and install the developer package.

Run **MySQL Command Line Client** and log in with your credentials.

Run these queries to create a database with the same name as is used in this project and initialize it.
```cmd
CREATE DATABASE receipy_testing;
use receipy_testing;
```
Given that everything went as intended, `cd` to the project folder and run `python manage.py migrate` to create the necessary database tables, and be synchronized with our project.

A `.env` file needs to be written to the root project folder.  It must contain your password, username and the name of the database.

```env
PASSWORD=yourPassword
USER=yourUser
NAME=databaseName
```

Finally, to be up-to-date on the Python packages used in the project, run `pip freeze > requirements.txt` to write a text file with the requirements, then run `pip install -r requirements.txt` to install
  * **Pip installation: https://pip.pypa.io/en/stable/installation/**

Start the project locally with `python manage.py runserver`
  * Database not running? search for **services.msc**, locate the database by the name you gave it, and run it.
