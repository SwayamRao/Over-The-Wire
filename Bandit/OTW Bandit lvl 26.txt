
We need to again bandit25 for this lvl.
In this lvl we first change shell for bandit26 and then access bandit26 through there.
For that we need to again exploit the 'more' command.
Then we need to set our shell for that.

-------------------------------
:set shell=/bin/bash
:shell
-------------------------------

:shell is used to access the shell as bandit26
Then we use ls to list the files present in bandit26 user
We use command :

-------------------------------
./bandit27-do cat /etc/bandit_pass/bandit27
-------------------------------

-------------------------------
Password : YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
-------------------------------
