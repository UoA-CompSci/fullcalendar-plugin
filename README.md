README
======

This project defines a plugin for the [Fullcalendar](http://fullcalendar.io/) JavaScript library that allows it to connect to the UoACalendar backend.

You may install this module using bower:

```bash
$ bower install fullcalendar-uoa --save
```

Dependencies
------------

Now you should have all the required js/css files. This includes the standard `fullcalendar.js` and `fullcalendar.css`, in addition to `uoacal.js`.

```
<link href="bower_components/fullcalendar/dist/fullcalendar.css" rel="stylesheet">
<link href="bower_components/fullcalendar/dist/fullcalendar.print.css" rel="stylesheet" media="print">

<script src="bower_components/jquery/dist/jquery.min.js"></script>
<script src="bower_components/moment/min/moment.min.js"></script>
<script src="bower_components/fullcalendar/dist/fullcalendar.min.js"></script>
<script src="bower_components/fullcalendar-uoa/uoacal.js"></script>
```

Writting the code
------------

It's time to initialize your calendar in JavaScript. You can do so as in this example:

```javascript
$(document).ready(function() {
    $('#calendar').fullCalendar({
        events: {
            uoaCalendarId: '<YOUR CALENDAR ID>',
            uoaCalendarApiToken: '<YOUR API TOKEN>',
            uoaCalendarHost: 'diaryapi.auckland.ac.nz',
            uoaCalendarPort: '345'
        }
    });
});
```

You may obtain an API token by logging into diaryapi.auckland.ac.nz then click your email address and select "API Token" from the menu. 

> Note that this will generate a new token and invalidate your old one if you already have one.

> After obtaining the token, please don't forget to close all browser windows to completely log out from diaryapi.auckland.ac.nz
