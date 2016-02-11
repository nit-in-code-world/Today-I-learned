# I/O Redirection

0, 1, and 2 represent the standard file descriptors in POSIX operating systems. A file descriptor is a system reference to a file or socket.

* 0 -> stdin
* 1 -> stdout
* 2 -> stderr


**/dev/null** indicates a empty device.

**&gt;** is used for output redirection.
**&gt;&gt;** is used for appending the redirected output to a file

**&lt;** is used for redirecting the input

**&** is used to tell the shell to run the command as a job in the background.
```
 /opt/dbeaver/dbeaver > /dev/null/ 2 >&1
 
 2>&1 indicates stderr is redirected to stdout, here & infront 1 indicates
 1 is not a file name but a file descriptor.
 
 hence the script dbeaver stdout and stderr are both redirected to null 
 device, indicating they are discarded.

```

References:

* [When to use STDERR instead of STDOUT](http://www.jstorimer.com/blogs/workingwithcode/7766119-when-to-use-stderr-instead-of-stdout)
* [Standard Input and Output Redirection](http://sc.tamu.edu/help/general/unix/redirection.html)
* [Unix - Shell Input/Output Redirections](http://www.tutorialspoint.com/unix/unix-io-redirections.htm)
