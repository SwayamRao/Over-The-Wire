In this lvl we have been given a text file with RSA private key.
We first try using ssh directly and use command :

-----------------------------
ssh bandit26@localhost -p 2220 -i bandit26.sshkey
-----------------------------

But we get disconnected immediately thats because the shell for user 26 is not /bin/bash as mentioned in question.
To find the shell on which user 26 is on we first do :

-----------------------------
cat /etc/passwd | grep bandit26
-----------------------------

We get the output as /usr/bin/showtext which is where we need to look for 

-----------------------------
cat /usr/bin/showtext 
-----------------------------

We get the shell script where we need to exploit the 'more' command to get normal shell.
First resize the screen to trigger the more command.
Then to launch text editor press 'v'.
Then type ":e /etc/bandit_pass/bandit26"

-----------------------------
Password : c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
-----------------------------

Reading material for more command : https://www.geeksforgeeks.org/more-command-in-linux-with-examples/
