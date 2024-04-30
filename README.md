# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
CLIENT
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
   msg=input("Client > ") 
   s.send(msg.encode()) 
   print("Server > ",s.recv(1024).decode())
```
SERVER
```
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    ClientMessage=c.recv(1024).decode() 
    c.send(ClientMessage.encode())
```
## OUPUT
![Screenshot 2024-04-30 085027](https://github.com/SAISANJAY10/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144228073/2cb30f63-9e3f-4b12-be0f-7936253c9d8b)
![Screenshot 2024-04-30 085041](https://github.com/SAISANJAY10/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144228073/a7e634fa-3778-4588-928a-9b38310489ec)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
