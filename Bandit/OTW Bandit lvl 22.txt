So in this lvl first we need to learn about understanding the shell scripts.
First we use command : 
  ls /etc/cron.d   to list the files present in etc/cron.d
then we notice that theres a file present in etc/cron.d and we print the contents of it using command :
 cat /etc/cron.d/cronjob_bandit23
We see a shell script running (which actually is daemon cron)
We can notice the shell script running on usr/bin/cronjob_bandit23.sh so we print the program using command : 
 cat /usr/bin/cronjob_bandit23.sh
{Understanding about the basic commands of linux and shell scripting would be helpful to understand }
Then use command : 
 myname=bandit23 
To change the myname value to bandit23 from bandit22.
Then use command :
  echo I am user $myname | md5sum | cut -d ' ' -f 1
You will get some output 
This output is actually a filename in temp directory {analyzing the shell script would be useful.}
Then use command : 
  cat /tmp/8ca319486bfbbc3663ea0fbe81326349 
to get the password

Password : QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G


