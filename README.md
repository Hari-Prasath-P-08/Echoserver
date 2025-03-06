# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:

#### NAME: HARI PRASATH. P
#### REG. NO: 212223230070

### Server Side:
```python
import socket
HOST = "127.0.0.1"  # Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)

```

### Client Side:
```python
import socket
HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Hello, world")
    data = s.recv(1024)
print(f"Received {data!r}")
```

## OUTPUT:

### Server Output:
![Screenshot 2025-03-06 113112](https://github.com/user-attachments/assets/7fdff48b-f614-428f-9ca7-1e179b303d7b)

### Client Output:
![Screenshot 2025-03-06 113120](https://github.com/user-attachments/assets/f1a7156b-d991-4f17-b997-a95999c34f64)

## RESULT:
The program is executed successfully
