README
======

This project defines a module for the `fullcalendar` JavaScript library that allows it to connect to the UoACalendar backend.

You may install this module using bower:

```bash
$ bower install fullcalendar-uoa --save
```

Dependencies
------------

Now you should have all the required js/css files. This includes the standard `fullcalendar.js` and `fullcalendar.css`, in addition to `uoacal.js`.

```
<script type='text/javascript' src='fullcalendar/dist/fullcalendar.min.js'></script>
<script type='text/javascript' src='fullcalendar-uoa/uoacal.js'></script>
```

Writting the code
------------

It's time to initialize your calendar in JavaScript. You can do so as in this example:

```javascript
$(document).ready(function() {
    $('#calendar').fullCalendar({
        uoaCalendarApiToken: '<YOUR API TOKEN>',
        uoaCalendarHost: 'calendar.auckland.ac.nz',
        uoaCalendarPort: '5000',
        events: {
            uoaCalendarId: '<YOUR CALENDAR ID>'
        }
    });
});
```

You may obtain an API token like this:

```bash
$ curl -X POST -d "username=<USERNAME>&password=<PASSWORD>" calendar.auckland.ac.nz:5000/api-token-auth
```

>> Note that this will generate a new token and invalidate your old one if you already have one.


