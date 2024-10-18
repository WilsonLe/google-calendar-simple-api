.. _change_log:

Change log
==========


v2.5.0
~~~~~~

API
---
* Consistent type annotations (primarily regarding `Optional`)
* Support python3.13

Core
----
* Include mypy as a PR check

Backward compatibility
----------------------
* Full compatibility


v2.4.0
~~~~~~

API
---
* Warn user about microseconds in start/end datetime
* Warn user about empty summary
* Adds open_browser argument to GoogleCalendar

Core
----
* None

Backward compatibility
----------------------
* If there is no available browser, by default, authentication will not raise an error and retry without the browser


v2.3.0
~~~~~~

API
---
* Adds `add_attendees` method to the `Event` for adding multiple attendees
* Add specific time reminders (N days before at HH:MM)
* Support Python3.12
* Allow service account credentials in `GoogleCalendar`

Core
----
* Don't evaluate default arguments in code docs (primarily for `timezone=get_localzone_name()`)

Backward compatibility
----------------------
* If token is expired but doesn't have refresh token, raises `google.auth.exceptions.RefreshError`
  instead of sending the request


v2.2.0
~~~~~~

API
---
* Adds support for new credentials file names (i.e. client_secret_*.json)

Core
----
* None

Backward compatibility
----------------------
* Full compatibility


v2.1.0
~~~~~~

API
---
* Adds support for python3.11
* Adds support for access control list (ACL) management
* Fix converting date to datetime in get_events
* Adds support for free/busy requests

Core
----
* None

Backward compatibility
----------------------
* Full compatibility

v2.0.1
~~~~~~

API
---
* Fixes issue with unknown timezones

Core
----
* Removes pytz dependency

Backward compatibility
----------------------
* Full compatibility


v2.0.0
~~~~~~

API
---
* Adds calendar and calendar list related methods
* Adds settings related method
* Adds colors related method
* Adds support for python3.10

Core
----
* Separates ``GoogleCalendar`` into authentication, events, calendars, calendar list, colors, and settings services
* Uses newest documentation generation libraries

Backward compatibility
----------------------
* Full compatibility


v1.3.0
~~~~~~

API
---
* Adds deletion of event by its id in ``GoogleCalendar.delete_event()``

Core
----
* None

Backward compatibility
----------------------
* Full compatibility


v1.2.1
~~~~~~

API
---
* Adds ``Event.id`` in serialized event
* Fixes conference's entry point without ``entry_point_type``

Core
----
* Switches to tox for testing

Backward compatibility
----------------------
* Full compatibility


v1.2.0
~~~~~~

API
---
* Adds ``GoogleCalendar.import_event()`` method

Core
----
* None

Backward compatibility
----------------------
* Full compatibility


v1.1.0
~~~~~~

API
---
* Fixes event creation without ``start`` and ``end``
* Adds ``creator``, ``organizer`` and ``transparency`` fields to event

Core
----
* None

Backward compatibility
----------------------
* Full compatibility


v1.0.1
~~~~~~

API
---
* Fixes ``GoogleCalendar.clear()`` method

Core
----
* None

Backward compatibility
----------------------
* Full compatibility


v1.0.0 and previous versions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

API
---
* Adds authentication management
* Adds event management
* Adds documentation in readthedocs.com

Core
----
* Adds serializers for events and related objects
* Adds automated testing in GitHub actions with code-coverage

Backward compatibility
----------------------
* Full compatibility