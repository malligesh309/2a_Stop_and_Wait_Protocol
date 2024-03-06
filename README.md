# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
### CLIENT:
```
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
### SERVER:
```
   import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
```
## OUTPUT:
### CLIENT:
![image](https://github.com/malligesh309/2a_Stop_and_Wait_Protocol/assets/140491043/71e3744a-57d0-4489-9381-0075cd2c2413)

### SERVER:

![Screenshot 2024-03-06 155547](https://github.com/malligesh309/2a_Stop_and_Wait_Protocol/assets/140491043/86b8ca71-d616-4676-9395-70fbcd8d91ca)


## RESULT
Thus,python program to perform stop and wait protocol was successfully executed Thus, python program to perform stop and wait protocol was successfully executed.
