## NAME:RAMYA P
## REGISTER NUMBER:212223230168

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
## CLIENT
~~~
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
~~~
## SERVER
~~~
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
~~~

## OUPUT
## CLIENT
![chat client](https://github.com/23006111/3b_CHAT_USING_TCP_SOCKETS/assets/145981696/872234d8-9f9c-4d09-97c9-c5b8d499e200)
## SERVER
![server chatt](https://github.com/23006111/3b_CHAT_USING_TCP_SOCKETS/assets/145981696/c396ad97-6e3c-42a6-b265-21b3c5574bfb)


## RESULT
Thus the python program for creating Chat using TCP Sockets Links was successfully created and executed.

