# Overview

Notes on the HTTP protocol.

# HTTP Headers

* To get the HTTP headers from a website enter:

  ```
  curl -I www.example.com
  ```
  This will display the header on the console

  Alternatively enter,

    ```
    wget --save-headers www.example.com
    ```

  This will download the HTTP return including the headers which has useful information, such as what web server the site is using.  In this case since no
  specific web page is requested it will likely create the default index.html file with the headers included.
