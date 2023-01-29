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
# Serializing
One of the main features needed by API systems is data "serialization" which is taking data from the code (Python) and converting it into something that can be sent through the network. For example, converting an object containing data from a database into a JSON object. Converting datetime objects into strings, etc.

Another big feature needed by APIs is data validation, making sure that the data is valid, given certain parameters. For example, that some field is an int, and not some random string. This is especially useful for incoming data.

Without a data validation system, you would have to do all the checks by hand, in code.

Serialization is the process of converting an object into a stream of bytes to store the object or transmit it to memory, a database, or a file. Its main purpose is to save the state of an object in order to be able to recreate it when needed. The reverse process is called deserialization.

```python
class Person(object):
    def __init__(self, id, name, birth_date):
        self.id = id
        self.name = name
        self.birth_date = birth_date
```

JSON only accepts native data types like integers, strings, booleans, and so on. It’s pretty clear that the Python json.dumps function on a Person object won’t work. Instead, we need a representation that only uses native data types before we can pass it to a JSON encoding function.

```python

def to_json(self):
    return {
        'id': self.id,
        'name': self.name,
        'birth_date': self.birth_date.isoformat(),
        'sidekick': self.sidekick.to_json() if self.sidekick else None,
    }
```
Python datetime object is not a native datatype and Person object which can’t be converted directly to JSON.


While this works, there are a few issues here. For one, we can’t define the field types. So if some code is consuming this JSON representation and we encounter a boolean value for id, the calling code would be confused. Ideally we would like to handle such cases already at serialization time. Additionally, some use cases might require that the returned value be different based on some context. As an example, consider a web application that allows chat rooms where two or more users can talk to each other. In such cases, the number of unread messages for the same chat room would be different based on which user is requesting the value.
An important thing to keep in mind is that serialization is not limited to JSON. There are plenty of other data formats (XML, for instance) which could use some help. Either way, the basic concept remains the same.

`serpy`
