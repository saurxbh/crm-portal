# crm-portal
A Customer Relationship Management Portal built using Python, Django and MySQL.

## Overview

This project is a CRM (Customer Relationship Management) application built using **Python**, **Django**, and **MySQL**. It provides full CRUD (Create, Read, Update, Delete) functionalities for managing customer data. The project also includes a Django superuser interface for admin-level management. The web app ensures a streamlined and efficient way to handle customer data.

## Features

- **CRUD Functionality**: Users can create, read, update, and delete customer data through Django views and forms.
- **Django Admin Interface**: Superuser privileges enable administrative management of the database.
- **Authentication & Authorization**: Secure login/logout functionality using Django’s built-in authentication system.
- **MySQL Database Integration**: Utilizes MySQL for efficient data storage and retrieval with optimized schema design.
- **Form Validation**: Django forms are used for both customer entries, ensuring input validation.
- **Responsive UI**: A clean, user-friendly interface optimized for desktops devices.

## Prerequisites

- **Python 3.x** and **pip** installed.
- **MySQL** installed and configured.
- **Virtualenv** for managing project dependencies.

## Setup Instructions

1. Clone the repository:

    ```bash
    git clone https://github.com/saurxbh/crm-portal.git
    ```

2. Create and activate a virtual environment:

    ```bash
    python -m venv env
    source env/bin/activate    # On Windows use `env\Scripts\activate`
    ```

3. Set up the MySQL database:
     
    - Install `mysqlclient` using `pip`.
    - Create a MySQL database for the project.
    - Configure the `DATABASES` setting in `settings.py` with your MySQL credentials.

5. Apply migrations to set up database schema:

    ```bash
    python manage.py migrate
    ```

6. Create a superuser for admin access:

    ```bash
    python manage.py createsuperuser
    ```

7. Run the development server:

    ```bash
    python manage.py runserver
    ```

8. Access the app:
   
    - Open a browser and go to `http://127.0.0.1:8000/` for the main application.
    - Admin interface available at `http://127.0.0.1:8000/admin`.

## Execution

- A superuser is created for secure admin access.
  ![image](/images/superuser1.png)
  ![image](/images/superuser2.png)
  ![image](/images/superuser3.png)
  ![image](/images/superuser4.png)


- New User can be registered by hitting the '/register' endpoint. The user has to fill out the registration form which is supported by Django's robust validation checks.
  ![image](/images/register-user.png)
  ![image](/images/register-user2.png)
  ![image](/images/register-user3.png)
  ![image](/images/register-user4.png)


- When the user logs in, all the records are displayed.
  ![image](/images/login.png)
  ![image](/images/login2.png)
  ![image](/images/get-all-users.png)


- A specific record can be viewed by clicking on the ID, which is the primary key.
  ![image](/images/get-user.png)


- A record can be updated by clicking on the 'Update' button, which hits the 'update/**id**' endpoint, where **id** is the ID of the record to be updated.
  ![image](/images/update.png)
  ![image](/images/update-user.png)
  ![image](/images/update-user2.png)
  ![image](/images/update-user3.png)


- A record can be deleted by clicking on the Delete button.
  ![image](/images/delete-user.png)
  ![image](/images/delete-user2.png)


- A new record can be created by clicking on the 'Add Record' button in the navbar. This links redirects to a form in which record details are to be entered.
![image](/images/add.png)
![image](/images/add-record.png)
![image](/images/add-record2.png)
![image](/images/add-record3.png)




![image](/images/logout.png)
![image](/images/persistence.png)
![image](/images/persistence2.png)


## Additional Notes

- The Django Admin interface provides complete control over all the data models, making management easy for administrators.
- The project uses Django's powerful ORM for database operations, making it scalable and efficient for handling large data sets.
