# django

## django manage command
see `commands.sh`


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

file-based sessions -> set SESSION_ENGINE settings to "django.contrib.sessions.backends.file"

****
One of the main features needed by API systems is data "serialization" which is taking data from the code (Python) and converting it into something that can be sent through the network. For example, converting an object containing data from a database into a JSON object. Converting datetime objects into strings, etc.

Another big feature needed by APIs is data validation, making sure that the data is valid, given certain parameters. For example, that some field is an int, and not some random string. This is especially useful for incoming data.

Without a data validation system, you would have to do all the checks by hand, in code.
