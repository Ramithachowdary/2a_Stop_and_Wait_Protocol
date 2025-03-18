# 2a_Stop_and_Wait_Protocol
## NAME: RAMITHA CHOWDARY S
## REG NO.: 212224240130
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
```
CLIENT: 
 
import socket 
s=socket.socket() 
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
```
SERVER: 
 
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    print(s.recv(1024).decode()) 
    s.send("Acknowledgement Recived".encode())
```

## OUTPUT
![Screenshot 2025-03-18 112403](https://github.com/user-attachments/assets/340ae6a8-54e1-4d37-a7cb-29c078dfa0b1)
![Screenshot 2025-03-18 112601](https://github.com/user-attachments/assets/469c215b-6968-4a3d-b377-85ff288ea4a1)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
