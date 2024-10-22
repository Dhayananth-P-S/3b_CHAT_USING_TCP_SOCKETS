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
## Client
```py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## Server
```py
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
## Client
![Screenshot 2024-10-22 092159](https://github.com/user-attachments/assets/2910ce74-f46a-4cc2-b784-74974348172c)
## Server
![Screenshot 2024-10-22 092215](https://github.com/user-attachments/assets/47547fbb-28ab-4de1-bb30-4680ab8e77c7)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
