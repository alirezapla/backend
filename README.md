# django

## django manage command

    ```python
        django-admin help - used to display usage information and a list of the commands provided by each application.
    
    ```

    ```python
        django-admin version - used to check your Django version.
    ```
    django-admin check - used to inspect the entire Django project for common problems.
    django-admin compilemessages - Compiles .po files created by makemessages to .mo files for use with the help of built-in gettext support.
    django-admin createcachetable - Creates the cache tables for use in the database cache backend.
    django-admin dbshell - Runs the command-line client for the database engine specified in your ENGINE setting(s), with the connection parameters (USER, PASSWORD, DB_NAME, USER etc.) specified settings file.
    django-admin diffsettings - Shows the difference between the existing settings file and Django’s default settings.
    django-admin dumpdata - Used to the dumpdata from the database.
    django-admin flush - Flush all values from the database and also re-executes any post-synchronization handlers specified in the code.
    django-admin inspectdb - It generates django models from the existing database tables.
    django-admin loaddata - loads the data into the database from the fixture file.
    django-admin makemessages - Used for translation purpose and it generates a message file too.
    django-admin makemigrations - Generates new migrations as per the changes detected to your models.
    django-admin migrate - Executes SQL commands after which the database state with the current set of models and migrations are synchronized.
    django-admin runserver - Starts a light-weight Web server on the local machine for development. The default server runs on port 8000 on the IP address 127.0.0.1. You can pass a custom IP address and port number explicitly if you want.
    django-admin sendtestemail - This is used to confirm email sending through Django is working by sending a test email to the recipient(s) specified.
    django-admin shell - Starts the Python interactive interpreter.
    django-admin showmigrations - Shows all migrations present in the project.
    django-admin sqlflush - Prints the SQL statements that would be executed for the flush command mentioned above.
    django-admin sqlmigrate - Prints the SQL statement for the named migration.
    django-admin sqlsequencereset - output the SQL queries for resetting sequences for the given app name(s).
    django-admin squashmigrations - Squashes a range of migrations for a particular app_label.
    django-admin startapp - Creates a new Django app for the given app name within the current directory or at the given destination.
    django-admin startproject - Creates a new Django project directory structure for the given project name within the current directory or at the given destination.
    django-admin test - Runs tests for all installed apps.
    django-admin testserver - Runs a Django development server (which is also executed via the runserver command) using data from the given fixture(s).
    django-admin changepassword - offers a method to change the user's password.
    django-admin createsuperuser - Creates a user account with all permissions(also known as superuser account).
    django-admin remove_stale_contenttypes - removes stale content types (from deleted models) in your database.
    django-admin clearsessions - Can be used to clean out expired sessions or as a cron job.

