# Studyrooms Booking Using Alma APIs

## Introduction

This web-based studyrooms booking  displays a calendar of studyrooms that allows patron and staff to view the bookings and loans (booked, claimed) in Alma. Also it allows them to book a study room if available.

## Requirements

This web-based application requires:

* [cURL](https://www.php.net/manual/en/book.curl.php)

## Configuration

For detailed documentation go to: 

For a video on how to use: 

To configure, edit the config.xml file as below: 

```
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<libraries>
<library>
<key>TST</key>
<apikey>l7xxb4d537794041495bb97a6111222333444</apikey>
<lib_code>TST</lib_code>
<adv_date>14</adv_date>
<lib_pickup_code>TST</lib_pickup_code>
</library>
<library>
<key>Library-Key-2</key>
<apikey>111222333444_API_Key2_555666777</apikey>
<lib_code>Library-Code-for-Opening-Hours</lib_code>
<adv_date>28-how-many-future-days-patron-can-book</adv_date>
<lib_pickup_code>Library-Pickup-Location-Code</lib_pickup_code>
</library>
</libraries>
```

And then you need a MMS ID of studyrooms, for example: 990000383740104322. 

You have 2 view pages:

Patron View: infex.php?key="Key of Library in config.xml file"&mms_id=990000383740104322

For example: https://your_site_domain.com/index.php?key=TST&mms_id=990000383740104322

(Patron view doesn't display patron names)

Staff View: staff.php?key="Key of Library in config.xml file"&mms_id=990000383740104322

For example: https://your_site_domain.com/staff.php?key=TST&mms_id=990000383740104322

(Staff view display patron names)

## Notes

- Viewers can pick a date to view bookings/loads of study rooms (by clicking on "Pick a date" button

- Viewers click and drag mouse to select times and then press enter (or click on "Book It" button) to book a study room

- Staff click on "Display Patron Names" button to view patron names of booked/loan rooms

## Maintainers/Sponsors

Current maintainers:

* [Simon H Mai](https://github.com/simonhm)
* Sonja Eilertson (documentation)

## License

[GPLv3](http://www.gnu.org/licenses/gpl-3.0.txt)
