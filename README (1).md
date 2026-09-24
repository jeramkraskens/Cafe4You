# Cafe4You 🍽️

Cafe4You is a PHP + MySQL restaurant website with customer features and an admin dashboard.

## Features

- User registration and login
- Browse food categories and menu items
- Add items to cart and place orders
- Table reservations
- Contact form
- User profile and order history
- Admin dashboard
- Manage categories, menu items, orders, reservations, users, and messages

## Requirements

Before running the project, install:

- XAMPP (Apache + MySQL)
- PHP 8.x recommended
- MySQL / MariaDB
- A web browser
- Git (optional, for cloning from GitHub)

## Setup Guide

### 1. Download or Clone the Project

If you are using Git:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Move the project folder into your XAMPP `htdocs` directory.

Example:

```text
C:\xampp\htdocs\Cafe4You
```

If the downloaded folder is named `Cafe4You-main`, you can keep that name or rename it to `Cafe4You`.

### 2. Start XAMPP

Open **XAMPP Control Panel** and start:

- Apache
- MySQL

Both services should show as running.

### 3. Create the Database

Open phpMyAdmin in your browser:

```text
http://localhost/phpmyadmin
```

Then:

1. Click **Import**.
2. Choose the `database_schema.sql` file from the project folder.
3. Click **Import / Go**.

The SQL file creates the database:

```text
restaurant_db
```

and creates the required tables and sample data.

### 4. Configure the Database Connection

Open:

```text
config/database.php
```

Update the database settings to match your local XAMPP/MySQL configuration.

Typical XAMPP configuration:

```php
private $host = "localhost";
private $database_name = "restaurant_db";
private $username = "root";
private $password = "";
```

> If your MySQL `root` user has a password, enter that password instead of leaving it empty.

### 5. Run the Website

If your folder is named `Cafe4You`, open:

```text
http://localhost/Cafe4You/
```

If your folder is named `Cafe4You-main`, open:

```text
http://localhost/Cafe4You-main/
```

The main page should now load.

## Admin Login

Open the normal login page:

```text
http://localhost/Cafe4You/login.php
```

Default admin account created by `database_schema.sql`:

```text
Username: admin
Password: password
```

After a successful admin login, you can access the admin dashboard.

Example:

```text
http://localhost/Cafe4You/admin/dashboard.php
```

## Customer Account

Customers can create an account from:

```text
http://localhost/Cafe4You/register.php
```

After registration, they can log in, add items to the cart, place orders, make reservations, and view their account information.

## Email Configuration

The project contains email-related configuration under:

```text
config/mail.php
```

If you want email features to work, update the mail/SMTP settings with your own credentials.

Do not upload real email passwords, app passwords, API keys, or other secrets to GitHub.

## Important Before Uploading to GitHub

Check configuration files for passwords or private credentials before pushing the project.

It is recommended to keep sensitive values out of the repository and use environment variables or a local configuration file where possible.

You can also add sensitive local files to `.gitignore`.

## Common Problems

### Database connection error

Make sure:

- MySQL is running in XAMPP.
- `restaurant_db` was imported successfully.
- The username/password in `config/database.php` are correct.

### Page not found

Make sure the project folder is inside:

```text
C:\xampp\htdocs\
```

and use the same folder name in your localhost URL.

### Apache does not start

Another program may already be using port 80 or 443. Check the XAMPP logs or change the Apache port.

### MySQL does not start

Check whether another MySQL service is already running, then review the XAMPP MySQL logs.

## Project Structure

```text
Cafe4You/
├── admin/
├── config/
├── images/
├── includes/
├── uploads/
├── add_to_cart.php
├── cart.php
├── checkout.php
├── contact.php
├── database_schema.sql
├── index.php
├── login.php
├── menu.php
├── orders.php
├── profile.php
├── register.php
├── reservations.php
└── README.md
```

## Technologies Used

- PHP
- MySQL / MariaDB
- HTML
- CSS
- JavaScript
- PHPMailer

## License

This project is intended for educational/project use. Add your preferred license here if you plan to distribute it publicly.
