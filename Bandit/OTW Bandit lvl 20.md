In this lvl we need to setup a server on any desried port.
For this we use netcat and we send the password of previous lvl so that the function suconnect gives us the pasword for this lvl.
We use command : echo "VxCazJaVykI6W36BkBU0mJTCM8rR95XT" | netcat -lp 1234 &
We use -l for listening and p for specifying the port
We use '&' so that the process runs in background.
Use command jobs to check for background process.
Then run the function on port 1234
 ./suconnect 1234

We get the password for the next lvl : NvEJF7oVjkddltPSrdKEFOllh9V1IBcq