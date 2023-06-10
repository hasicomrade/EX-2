# EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL

## DATE: 15.03.2023
## AIM :

To write a python program to perform stop and wait protocol 
## ALGORITHM :

1.Start the program. 2.Get the frame size from the user 3.To create the frame based on the user request. 4.To send frames to server from the client side. 5.If your frames reach the server it will send ACK signal to client otherwise it will sendNACK signal to client. 6.Stop the program
## PROGRAM :
## CLIENT :
```
#Developed by : Harshini S
#Register Number : 212221220018
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
 print(ack)
 continue
 else:
 c.close()
 break
```
## SERVER :
```
#Developed by : Harshini S
#Register Number : 212221220018
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Received".encode())
```
## OUTPUT :
## CLIENT:
![image](https://github.com/hasicomrade/EX-2/assets/129851449/5637fbf5-bfbe-45fd-85d6-116bcf29fc02)

## SERVER:
![image](https://github.com/hasicomrade/EX-2/assets/129851449/1859fa90-34b5-4ef7-8e59-db7c0d995dea)

## RESULT :

Thus, python program to perform stop and wait protocol was successfully executed.
