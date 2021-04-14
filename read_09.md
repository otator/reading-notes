# WRRC and Java
## HTTP Request
### Local Processing
the http request that send using the browser has the following:
* _protocol_ which is HTTP in this case follwed by **://**
* _host_ for example (www.example.com)
* _port_ number (25000)
* _path_ to the file
* _query_ parameters
full request seems like -> http://www.example.com:25000/mainPage/query1=param1

the browser extact the host then try to get the ip for the host
it will check the local router's cache and the DNS local cache

### Resolve IP
if the first request fails to return an address, then the browser will try to get the ip from the DNS server.

the browser will use UDP protocol(ligh wight but it does not gurantee acknowledgment) to send the host name to DNS server to get the ip for that host.

if the DNs server fails to get the ip it will redirect the request to another DNS server(preconfigured in the DNS server) to check if the host is rigestered in that DNS server, if the last one fails will redirect the request also to another DNS sever until the host resolved to an ip, if all the DNS server fail to resolve the ip, failure respone will be sent to the browser and the browser will show error in opening the website.

*if the ip resolved the browser will cache the infromation to its cache memory in order for later requests. so that the browser will get the ip from its cache.*

### Establish a TCP Connection
once the broswer get the ip for the host, it will send a request to that host using TCP potocol,this protocol gurantee acknowledgment, this means every byte sent from the host to the browser is being guranteed that recived, this protocol using three-way handshake by sending sequence numbers of the bytes between the host and the browser.

### Send an HTTP Request
once the tcp connection between the host and the browser is open, an  http request can be sent, the http request has header and body, the header has the method of http such GET, POST, PUT...etc.


and once the host recieves the request it will generate a response to be sent to the browser, this response has status code that indicates whether the request success, failure or error state.

### Tearing Down and Cleaning Up
when the response has fully delivered to the browser, it will send FIN packet to the host ensures that the content was fully delivered and the host will send FIN packet to the browser.

there is a delay time before the connection is closed in order to get all the delayed packages from the host.




