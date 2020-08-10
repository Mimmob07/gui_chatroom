# Gui_chatroom
![Image of chatroom](chatroomex.png)
Its a chatroom with a Gui login, the login is all mine but the chatroom has some inspiration from stackoverflow
# Instalation
```
$ git clone https://github.com/thepythonscript/gui_chatroom
```
# Running the server
```
$ ./server
```
If that doesnt work try:
```
$ python(3) server
```
# Running and using the Client
### Running the Client
```
$ ./chatroom
```
### Using the Client
![Image of client](loginex.png)
Right now you cant create a new user in the program you can only hard code it into the `login_info.txt`
like this 
> note that the `Return` key is Binded to login on server ip
```
$ nano .files/login_info.txt
```
> inside nano
```
{"test_user" : "password"}
```
and change it to
```
{"test_user" : "password", "your_user" : "your_password"}
```
### Variables
```python
RECORD_MESSAGE = False
PREVIOUS_UNAME = True
PREVIOUS_IP = True
```
You can change the variables like if you change `RECORD_MESSAGE` to `True` then it will save all the messages to .files/messages.txt including a time stamp. the other ones just save previous answers.
# Bot Commands
### !serverip
When you type `!serverip` it returns whatever the servers ip adress was
### !localip
When you type `!localip` it returns your ip adress
### !help
the `!help` command returns:
```
server commands:
!serverip		returns server ip adress
!localip		returns local ip adress
!raven			Starts raven-storm
Note: whatever the bot returns does not get sent to the others
````
# ToDo
- [x] Make a create user page
- [x] Make a settings page
- [x] Make bot commands
