# Introduction

Thank you for choosing Droppy! This documentation will guide you through the installation, configuration, and usage of Droppy. If you have any questions or require further assistance, please don't hesitate to contact our support team at [support@proxibolt.com](mailto:support@proxibolt.com).

# Table of Contents

1. [Quick Start](#quick-start)
   - [Installation](#installation)
   - [Uploading Files](#uploading-files)
2. [Getting Started](#getting-started)
   - [Requirements](#requirements)
   - [Installation](#installation-1)
   - [Configuration](#configuration)
3. [Settings](#settings)
   - [General Settings](#general-settings)
   - [Email Settings](#email-settings)
   - [Email Templates](#email-templates)
   - [Social Settings](#social-settings)
4. [Translations](#translations)
5. [Troubleshooting](#troubleshooting)
   - [White Screen Issue](#white-screen-issue)
   - [Missing Files Issue](#missing-files-issue)
6. [Frequently Asked Questions](#frequently-asked-questions)
7. [Contacting Support](#contacting-support)

# Quick Start

## Creating a Database with phpMyAdmin

To create a database using phpMyAdmin, follow these steps:

1. Open phpMyAdmin in your web browser.
2. Login to phpMyAdmin using your credentials.
3. Once logged in, you will see the phpMyAdmin interface. On the left side, you will find a panel displaying the existing databases.
4. Locate the section labeled "Create new database" or similar. This is where you can create a new database.

5. Enter a name for your database in the provided field. Choose a name that is descriptive and relevant to your application or project.

6. Click the "Create" button to create the database.

7. phpMyAdmin will confirm the successful creation of the database. You should now see the newly created database in the list on the left side.

### Creating a database (video)
For a visual demonstration of the process, you can watch this YouTube video: [Creating a Database](https://www.youtube.com/watch?v=Y7ZVWQFOuDQ)

## Video of the installation
A video of the steps that are mentioned below is also available over here [Droppy V2 Installation](https://youtu.be/p2ukqE7vEzo)

## Installation

To install Droppy, please follow these steps:

1. Unzip the "Files" directory.
2. Open the `application/config/database.php` file and enter your database connection settings. Save the file.
3. Upload all the files from the "Files" directory to your server, including the modified `database.php` file.
4. Open your web browser and visit `http://yourwebsite.com/install`.
5. Follow the installation steps provided.
6. Once the installation is complete, you can log in to the admin panel using the login details you entered during installation.
7. Customize the settings according to your requirements.
8. Create a cron job that points to the URL `http://yourdomain.com/cron` to enable automated tasks. Refer to the tutorial on managing cron jobs with PHP for assistance.

## Uploading Files

To upload files using Droppy, follow these steps:

1. Click the "Select file(s)" button and choose the files you want to upload.
2. Enter the email addresses of the recipients you want to send the file(s) to. If you don't want to send via email, skip to step 4.
3. Enter your email address. If you don't want to send via email, skip to step 4.
4. Enter a message that you want to send to the recipients.
5. To access additional upload options, click the gear icon in the bottom right corner.
6. Adjust the maximum upload size by navigating to **Settings -> General Settings** in the admin panel.

# Getting Started

## Requirements

Before using Droppy, ensure that you have the following requirements:

- MySQL database
- Recommended PHP version (latest)
- mod_rewrite enabled
- Access to cron jobs

## Installation

To install Droppy, perform the following steps:

1. Create a database by following the tutorial using phpMyAdmin.
2. Unzip the "Files" directory.
3. Open the `application/config/database.php` file with a text editor.
4. Update the following values in the `database.php` file:
   - Replace `#db_host#` with your host address.
   - Replace `#db_username#` with your database username.
   - Replace `#db_password#` with your database password.
   - Replace `#db_name#` with your database name.
5. Upload all the files from the unzipped folder to your web server directory, including the modified `database.php` file.
6. Access your browser and enter a URL like `http://yourwebsite.com/install`.
7. Follow the provided installation steps.
8. After installation, remove the `application/controllers/Install.php` file from your server.
9. Log in to the admin panel using the login details you provided during installation. The admin panel URL is `http://yourwebsite.com/admin`.
10. Change the directory permissions of the `uploads/` directory to allow write access.
11. Set up a cron job to run the URL `http://yourdomain.com/cron` at regular intervals (1 to 5 minutes). Refer to the tutorial on managing cron jobs with PHP for assistance.

# Settings

## General Settings

In the general settings section, you can customize the following:

- **Site name**: The name of your website, displayed in emails and headers.
- **Site title**: The title of your website, shown in browser tabs and used by search engines.
- **Site description**: A description of your website, used by search engines like Google.
- **Logo path**: The path to the logo image displayed on the Droppy home page. Use `../` to go up a directory.
- **Favicon path**: The path to the favicon image displayed in the browser tab. Use `../` to go up a directory.
- **Backgrounds**: The path to the background image displayed on the Droppy home page. Use `../` to go up a directory.
- **Language**: The path/name of your language file. Default is `English.php`, but you can change it to a different file in the `config/language/` directory.
- **Expire time**: The duration before files are automatically destroyed. Requires a configured cron job.

## Email Settings

In the email settings section, you can configure the following:

- **Email from**: The email address from which emails are sent, e.g., `noreply@proxibolt.com`.
- **Email from name**: The name of the sender for outgoing emails, e.g., No-Reply Proxibolt.
- **Email server**: Choose between using the local email server or an external SMTP server.

## Email Templates

In the email templates section, you can customize the messages sent via email. Use variables to output dynamic values.

- **E-Mail receivers**: The email message sent to file recipients.
- **Email sender**: The email message sent to the file sender.
- **Email destroyed**: The email sent to the sender when their file(s) have been destroyed.
- **Email file downloaded**: The email sent to the sender when a recipient downloads the file.

## Social Settings

In the social settings section, you can add links to your social media accounts. Leave a field empty to hide the corresponding link on the home page.

# Translations

To translate Droppy into your language, follow these steps:

1. Duplicate the `english` directory located in `application/language/` and rename it to your language, e.g., `dutch`.
2. Open the language directory you created and edit the PHP files inside. Replace the English sentences with translations in the text after the arrow (`->`).

# Troubleshooting

## White Screen Issue

If you encounter a white screen when accessing your Droppy website, please ensure that you have installed Droppy correctly and that all seven required database tables exist.

## Missing Files Issue

If the upload process completes successfully but the files do not exist on your server, check the permissions of the `uploads/` directory. It should have write permission (777 or 0777).

# Frequently Asked Questions

For answers to frequently asked questions, please refer to our [FAQ](http://support.proxibolt.com/hc/en-us/categories/200495571-Support) section.

# Contacting Support

If you encounter any other issues or require further assistance, please contact our support team at [support@proxibolt.com](mailto:support@proxibolt.com).

Thank you for choosing Droppy as your self-hosted PHP upload file sharing platform. We hope this documentation helps you get started and make the most of Droppy's features. If you have any feedback or suggestions, please let us know.