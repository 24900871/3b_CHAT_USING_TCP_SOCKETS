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

CLIENT : 
~~~

import socket 
s=socket.socket() 
s.connect(('localhost',8002)) 
while True: 
     msg=input("Client > ") 
     s.send(msg.encode()) 
     print("Server > ",s.recv(1024).decode())

~~~
SERVER: 
~~~

import socket 
s=socket.socket() 
s.bind(('localhost',8002)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
             ClientMessage=c.recv(1024).decode() 
             print("Client > ",ClientMessage) 
             msg=input("Server > ") 
             c.send(msg.encode()) 

~~~

## OUPUT

CLIENT :

![image](https://github.com/user-attachments/assets/df26fa52-7e31-4e90-b75d-87744fa8af2f)

SERVER :

![image](https://github.com/user-attachments/assets/880606f0-6c7c-4df5-844d-b27f134a397d)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
