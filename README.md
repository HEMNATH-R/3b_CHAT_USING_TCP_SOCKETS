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
# Client:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
# Server:
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
# Client:
<img width="690" height="227" alt="image" src="https://github.com/user-attachments/assets/f2b3c3b8-bfb6-4666-a67b-81cca070654b" />


# Server:
<img width="689" height="218" alt="image" src="https://github.com/user-attachments/assets/9230b967-6a5b-4746-892c-f44bfd34556f" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
