# CGI-cpp-parser-for-stdin
Reading and writing  CGI coding  in C or C++ to  parser  STDIN.  

Reading the Input

The first thing your script must do is determine its environment. The server will invoke your script with one of several request methods-GET, POST, PUT, or HEAD-and your script must respond accordingly.

The server tells you which request method is being used via an environment variable called, appropriately enough, REQUEST_METHOD. Your script should use getenv("REQUEST_METHOD") to retrieve the value of this variable. The value will be a character string spelling out GET, POST, PUT, or HEAD.

NOTE

    PUT and HEAD are almost never used for CGI (their actions are undefined for CGI), and I won't discuss them here. 

    However, although you'll probably never encounter a situation where your program is invoked with a request method other than GET or POST, you should always check the value of REQUEST_METHOD carefully. It's not safe to assume that if the method isn't GET that it must be POST, or vice versa 
