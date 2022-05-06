# 👨‍💻 mitm

<p align="center">

This is an implementation to use mitm for https automatically.

Note that OpenSSL installed in your path is required.

  All the code is implemented in the main.py file. 
It has the HttpsLogger class that implements everything needed for https to work on windows. 
It creates a ca cert when the mitm starts, and installs it to the your system(for windows only)
Every time a new host logs in a new cert is created and signed by our root CA. 
To use this object just create a new one and implement the write function for the way you want to log your info or change the each function if you want to change the data or log it in other way. 
There is two examples to how to use it with file logging or with sockets

The function netstart and filestart starts the proxy in your system as well (in windows only)

Note that the code must run in administrator mode. 
