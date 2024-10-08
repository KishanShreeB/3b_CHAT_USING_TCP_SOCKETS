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
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
  msg=input("Client > ")
  s.send(msg.encode())
  print("Server > ",s.recv(1024).decode())

## SERVER
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

## OUPUT
![image](https://github.com/user-attachments/assets/8e57bb6f-7281-4b79-b30c-6218f75e8e6c)
![image](https://github.com/user-attachments/assets/13123387-f32d-4376-a7f5-3b9ac718e4b4)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
