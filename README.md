# Google Calendar Simple API

Simple adapter for https://github.com/googleapis/google-api-python-client

Example usege:

    from beautiful_date import *
    from gcsa import GoogleCalendar, Event, rule, DAILY
    
    calendar = GoogleCalendar('kuzmovich.goog@gmail.com')
    event = Event(summary="Breakfast", start=12/Dec/2018, recurrence=rule(freq=DAILY))
    calendar.add_event(event)
    
    ...
    
    for event in calendar.get_events():
        print(event.start, event.summary)

The idea is to keep all the functionality of the original API, but simplify implementation of the most popular cases.


![alt tag](http://alfaraj-group.com/wp-content/uploads/2016/09/underConstruction.png)

