# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
1.SERVER:
```python
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

2.CLIENT:
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## OUPUT:
1.SERVER:

![cn  3b](https://github.com/user-attachments/assets/0f72767c-45f8-4c6c-a15d-7215aa26df5f)

2.CLIENT:

![cn 3b](https://github.com/user-attachments/assets/d7cd2df1-e131-4e92-84af-6e159c39d164)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
