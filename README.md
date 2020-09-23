<div align="center">

## ^\!\!\~ Check if a service/machine is alive \~\!\!^


</div>

### Description

Check and see if a service is up or down on a certain machine.

Useful for alot of things, say you have MSN Messenger or AIM, you can have a script check YOUR IP address and the MSN or AIM port number and then let the users at your website know if your online or not! Can also be useful if you use alot of file mirrors for your website and want to check if there up or down. Infinite amount of uses! Really fun, simple, easy to use, and useful for many things. Well commented.
 
### More Info
 
$address, $service

Don't forget to change $address and $service, doh!

If you forget to turn off error reporting(error_reporting(0);), you will get a 'Warning' if fsockopen fails to connect.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[fritz0x00](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/fritz0x00.md)
**Level**          |Advanced
**User Rating**    |4.3 (26 globes from 6 users)
**Compatibility**  |PHP 3\.0, PHP 4\.0
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__8-1.md)
**World**          |[PHP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/php.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/fritz0x00-check-if-a-service-machine-is-alive__8-1354/archive/master.zip)





### Source Code

```
<?php
error_reporting(0); //** Turn error reporting off so we don't get the unneeded warning message if we fail to connect, we will handle that our selfs
$address = "127.0.0.1"; //** Address of the machine
$service = 80; //** Service or Port number, in this case 80 for the HTTPD daemon... say we want to have a page to check if our webserver is up
//** fsockopen returns a boolean value upon execution, depending if it fails(returns FALSE or NULL) or not(returns TRUE)
if(fsockopen($address, $service)) //** If we can connect...
{
 //** Address is up, do what you want here
 echo "$address:$service is up!";
}
else //** We can't connect!
{
 //** Address is NOT up, do what you want here
 echo "$address:$service is NOT up!";
}
?>
```

