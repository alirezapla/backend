# django

## django manage command

```python
django-admin help #- used to display usage information and a list of the commands provided by each application.

```

```python
django-admin version #- used to check your Django version.
```
```python
django-admin check #- used to inspect the entire Django project for common problems.
```
```python
django-admin compilemessages #- Compiles .po files created by makemessages to .mo files for use with the help of built-in gettext support.
```
```python
django-admin createcachetable #- Creates the cache tables for use in the database cache backend.

```
```python
django-admin dbshell #- Runs the command-line client for the database engine specified in your ENGINE setting(s), with the connection parameters (USER, 
#PASSWORD, DB_NAME, USER etc.) specified settings file.
```
```python
django-admin diffsettings #- Shows the difference between the existing settings file and Django’s default settings.
```
```python
django-admin dumpdata #- Used to the dumpdata from the database.
```
```python
django-admin flush #- Flush all values from the database and also re-executes any post-synchronization handlers specified in the code.
```
```python
django-admin inspectdb #- It generates django models from the existing database tables.
```
```python
django-admin loaddata #- loads the data into the database from the fixture file.
```
```python
django-admin makemessages #- Used for translation purpose and it generates a message file too.
```
```python
django-admin makemigrations #- Generates new migrations as per the changes detected to your models.
```
```python
django-admin migrate #- Executes SQL commands after which the database state with the current set of models and migrations are synchronized.
```
```python
django-admin runserver #- Starts a light-weight Web server on the local machine for development. The default server runs on port 8000 on the IP address 127.0.0.1. You can pass a custom IP address and port number explicitly if you want.
```
```python
django-admin sendtestemail #- This is used to confirm email sending through Django is working by sending a test email to the recipient(s) specified.
```
```python
django-admin shell #- Starts the Python interactive interpreter.
```
```python
django-admin showmigrations #- Shows all migrations present in the project.
```
```python
django-admin sqlflush #- Prints the SQL statements that would be executed for the flush command mentioned above.
```
```python
django-admin sqlmigrate #- Prints the SQL statement for the named migration.
```
```python
django-admin sqlsequencereset #- output the SQL queries for resetting sequences for the given app name(s).
```
```python
django-admin squashmigrations #- Squashes a range of migrations for a particular app_label.
```
```python
django-admin startapp #- Creates a new Django app for the given app name within the current directory or at the given destination.
```
```python
django-admin startproject #- Creates a new Django project directory structure for the given project name within the current directory or at the given destination.
```
```python
django-admin test #- Runs tests for all installed apps.
```
```python
django-admin testserver #- Runs a Django development server (which is also executed via the runserver command) using data from the given fixture(s).
```
```python
django-admin changepassword #- offers a method to change the user's password.
```
```python
django-admin createsuperuser #- Creates a user account with all permissions(also known as superuser account).
```
```python
django-admin remove_stale_contenttypes #- removes stale content types (from deleted models) in your database.
```
```python
django-admin clearsessions #- Can be used to clean out expired sessions or as a cron job.
```


## Signals

List of built-in signals in the models:


| Signals |	Description|
| :---: | :---: | 
|django.db.models.pre_init & django.db.models.post_init 	| Sent before or after a models’s _init_() method is called |
|django.db.models.signals.pre_save & django.db.models.signals.post_save 	| Sent before or after a model’s save() method is called |
|django.db.models.signals.pre_delete & django.db.models.signals.post_delete |	Sent before or after a models’ delete() method or queryset delete() method is called |
|django.db.models.signals.m2m_changed |	Sent when a ManyToManyField is changed |
|django.core.signals.request_started & django.core.signals.request_finished |	Sent when an HTTP request is started or finished |


****


Some of the caching strategies in Django are listed below:

|Strategy |	Description |
| :---: | :---: | 
|Memcached |	A memory-based cache server is the fastest and most efficient |
|FileSystem Caching |	Values of the cache are stored as separate files in a serialized order|
|Local-memory Caching |	This is used as the default cache strategy by Django if you haven’t set anything. It is per-process as well as thread-safe.|
|Database Caching | 	Cache data will be stored in the database and works very well if you have a fast and well-indexed DB server.|

