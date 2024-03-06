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
### CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUPUT
### CLIENT
![image](https://github.com/Thilak45/3b_CHAT_USING_TCP_SOCKETS/assets/138849161/9c8ba2c3-e4a8-49f4-a0c1-c9abb2e99150)
### SERVER
![image](https://github.com/Thilak45/3b_CHAT_USING_TCP_SOCKETS/assets/138849161/95f975de-43ae-404a-b5ba-a2dbc7a75783)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
