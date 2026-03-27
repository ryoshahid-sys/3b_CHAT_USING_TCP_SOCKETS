# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
```
SERVER 
import socket 
s = socket.socket() 
s.bind(('localhost', 8000)) 
s.listen(1) 
c, _ = s.accept() 
while True: 
print("Client >", (msg := c.recv(1024).decode())) 
c.send(input("Server > ").encode()) 
CLIENT 
import socket 
s = socket.socket() 
s.connect(('localhost', 8000)) 
while True: 
s.send((msg := input("Client > ")).encode()) 
print("Server >", s.recv(1024).decode())
```
## OUPUT

<img width="883" height="320" alt="image" src="https://github.com/user-attachments/assets/e58153c7-3c2d-4b37-a0e4-b871c975e8ef" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
