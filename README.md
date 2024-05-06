# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Name:Vedagiri Indu Sree
## Reg no:212223230236
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## Client:
```
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## Server:
```
import socket
s=socket.socket()
s.bind(('localhost',800))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUPUT
## Client:
![image](https://github.com/vedagiriindusree/3b_CHAT_USING_TCP_SOCKETS/assets/149366776/3bf60dda-6acb-4aad-b3dc-c44acb9c4b32)
## Server:
![image](https://github.com/vedagiriindusree/3b_CHAT_USING_TCP_SOCKETS/assets/149366776/891c1143-dffd-4aaf-bc02-1be94ef076b0)
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
