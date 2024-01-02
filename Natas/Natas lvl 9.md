In this lvl we first view the source code as usual.
We find that there's a php source code provided.
We can see that the key is a variable and the if statement looks for variable named needle in the request.
So when we give needle, make sure to observe the search box.
Now there is execution of the code 
   passthru("grep -i test dictionary.txt");
Here we can do command injection to get into the root directory and get the password.
----------------------------------------
Password : D44EcsFkLxPIkAAKLosx8z3hxX1Z4MCE
----------------------------------------
Reading material : https://portswigger.net/web-security/os-command-injection
