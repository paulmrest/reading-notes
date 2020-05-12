# Read 13 - Local Storage

## [Local Storage - Dive into HTML5](http://diveinto.html5doctor.com/storage.html)

Despite the article being from 2011 (and still using HTTP!) this was a really good read. I actually enjoyed this much more than the Duckett textbooks.

Really my take-away is that HTML5 introduced a unified way for browsers to store data on user's machines, **HTML5 Local Storage**. Data is stored in key/value pairs, and all data is stored as strings (much like Objective-C's CoreData). Browsers at the time of the article gave 5 MB of storage space per site, and while a user could manually increase that size, a web site cannot increase its own storage.

Generally one checks if a web browser supports storage, and then can set and get data as required.

There are (were?) other possible future protocols, one of which is built around a SQL varient, and another called **Indexed Database API** that uses an **object store**.