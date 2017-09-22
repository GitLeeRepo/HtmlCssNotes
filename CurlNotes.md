# Overview

Notes on the curl command line tool for transferring data via a number of protocols, including HTTP, IMAP, POP3, FILE, FTP, etc.  It is open source, it can be found on Linux distros, MacOS, and on Windows using something such as Git Bash.  Here is the 
[main website](https://curl.haxx.se/).

# Commandline options

* Test site

The curl examples here are run agains the [JSONPlaceholder site](https://jsonplaceholder.typicode.com/) test site, which is a good site for testing JSON/AJAX and REST API.

* Without paramaters or filters

```
curl https://jsonplaceholder.typicode.com/posts/
```
This returns all 100 of the test post JSON objects from the site

* Filter for just id:2

```
curl https://jsonplaceholder.typicode.com/posts/2
```
This returns all 100 of the post test JSON objects from the site

* Include HTTP header info along with the rest of the data

```
curl -i https://jsonplaceholder.typicode.com/posts/
```

* Include just the HTTP header

```
curl -I https://jsonplaceholder.typicode.com/posts/
```

* Download content to a specific file

```
curl -o test01.json https://jsonplaceholder.typicode.com/posts/
```

