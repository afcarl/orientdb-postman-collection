# orientdb-postman-collection
A complete postman collection for OrientDB HTTP API

OrientDB Version: 2.2.X
Postman Collection Format: v2

# How to use
- Import both the collection and environment json file into Postman.
- Select the imported "OrientDB HTTP API env" from environment selections.
- Make necessary modifications to the environment variables to suit your need (e.g. host, port, database)
- Now you are set. Try to make a request from the "OrientDB API Sample" collection.

# Description
This is a manually typed and tested postman collection matches the official OrientDB RESTAPI document(ver.2.2.X)
It covers all materials from the document
http://orientdb.com/docs/2.2.x/OrientDB-REST.html

# Quicknotes About Authorization
- OrientDB RESTAPI is using session for user authorization, which means you may not necessary include Authorization header in any of the following requests before a session is expired (300s by default), so it is recommanded to use 'GET - Connect' request to establish a session before making any other requests.

- You can surely include Authorization header in every request made in production.

- [EXCEPTION] Some of the requests requires 'root' user authorization instead of a database user like 'admin', so you may be needed to include proper authorization header for those requests (e.g. Database and Server related requests).