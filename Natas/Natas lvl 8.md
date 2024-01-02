In this lvl we first get a query submission and if its correct then will get the password for next lvl.
After seeing the source code, we can understand that the secret is being manipulated.
This function of php shows the manipulation:

   $encodedSecret = "3d3d516343746d4d6d6c315669563362";

  function encodeSecret($secret) {
    return bin2hex(strrev(base64_encode($secret)));
 } 
 {bin2hex is used to convert ascii to hex }.
 We can understand that the encodedSecret is the manipulated code and we need to get the original code to submit.
 So I wrote a CODE in php to do the reverse manipulation of the manipulated code. {Ik it sounds confusing cause i made it confusing lol}
 The CODE :
  
 $encodedSecret = "3d3d516343746d4d6d6c315669563362";
  echo base64_decode(strrev(pack("H*",$encodedSecret)))

here pack() is used to convert from hex to ascii
After this we get the code : oubWYf2kBq
Enter this to get the password
---------------------------------
Password : Sda6t0vkOPkM8YeOZkAGVhFoaplvlJFd
---------------------------------
