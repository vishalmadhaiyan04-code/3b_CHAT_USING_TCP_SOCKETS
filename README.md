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
# SERVER
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
# CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8000))

while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## OUPUT

<img width="448" height="157" alt="image" src="https://github.com/user-attachments/assets/8b2bfe14-c675-4356-b0ea-7f4c67f17167" />

<img width="482" height="199" alt="image" src="https://github.com/user-attachments/assets/86ab0bd7-7494-4489-9100-1d3ee3142f38" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
