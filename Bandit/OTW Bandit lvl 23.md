
Firstly we try to list out the things present in /etc/cron.d.
Then we cat the file /etc/cron.d/cronjob_bandit24.
We see that there's an script running named cronjob_bandit24.sh.
then we cat that script using the command : 
 cat /usr/bin/cronjob_bandit24.sh
After analyzing the script ,

 [ "$i" != "." -a "$i" != ".." ]; 

This basically means to ignore the . and .. directory which are current directory and parent directory.

if [ "${owner}" = "bandit23" ]; then

This is used to check if the owner variable is equal to bandit23.

timeout -s 9 60 ./$i

If yes then run the script after 60 sec timeout.

Then make a temp directory in /tmp
and change permission so that bandit23 can access the file.
then write a shell script :
cat /etc/bandit_pass/bandit24 > /tmp/john/pass.txt

Then wait for the 60 sec delay and check the pass.txt file to get password.

Password : VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar