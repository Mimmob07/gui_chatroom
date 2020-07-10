# Introduction
This markdown(.md) file is going to describe how the code works(how the sockets connect, how the login works, etc)
# How the sockets connect
![img ex of sockets](https://i1.wp.com/slacker.ro/wp-content/uploads/2019/08/python-socket-connection-diagram-00.png?resize=1360%2C765&ssl=1)
### The code
```python
import socket

def echo_data(sock):
   while True:
      try:
         msg = sock.recv(1024).decode('utf8')
         msg_list.insert(tk.END, msg)
      except OSError:
         break

address = (host,port)
s.connect(address)

threading.Thread(target=echo_data, args = (s,)).start()
```
### The explination
`import socket` is obviosly the most important(without it we couldnt do anything)
```python
def echo_data(sock):
   while True:
      try:
         msg = sock.recv(1024).decode('utf8')
         msg_list.insert(tk.END, msg)
      except OSError:
         break
```
this part recives the data from the server
(this is the exact line that recives the data `msg = sock.recv(1024).decode('utf8')`)
```python
address = (host,port)
s.connect(address)
```
this part makes the actual connection to the server
