To run my code, have the httpserver.cpp file in your directory and use make to
get an executable version of it. You can type ./httpserver "hostname" "port" to open the socket
for the server. The hostname and port will be dependent on what you enter in to the console.
To connect via the client, establish a connection to the server with a curl command with flags:
"-s -T" "-s" to set up a GET or PUT message request.
For example:
curl -s http://127.0.0.1:8888/blah --request-target ABCDEFarqdeXYZxyzf012345-ab
-taken from CSE130 piazza post number 154
This will initiate a GET request from the client at host 127.0.0.1 and port 8888 for the
target file ABCDEFarqdeXYZxyzf012345-ab.
Users will have to note that valid resource names must be exactly 27 characters and only be alpha-numeric characters or "-" or "_"
It will give a bad request otherwise.
This program will not be able to handle requests other than GET or PUT.
