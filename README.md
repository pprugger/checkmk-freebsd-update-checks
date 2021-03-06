# FreeBSD Update Checks for checkmk

This checkmk local checks enable your checkmk server to check the update state of FreeBSD servers.


Dependencies:
* bash

# Pull Requests
If you find errors in the scripts, feel free to create pull requests.


# Installation
* If you don't have bash installed, install it
* Copy the scripts to /usr/lib/check_mk_agent/local/ on the FreeBSD server
* Make the scripts executable with chmod +x script
* Run a full service scan on the host in checkmk
* Add the new service to the monitored services


## Cached execution
It is advised to cache the output of the checks and not run them every minute.  
To do this generate a folder in /usr/lib/check_mk_agent/local/ and move the scripts there before you run the full service scan.  
The folder is named as the time in seconds the checks should run.  

For example if you want to run the checks every 600 seconds this path should do it:  
/usr/lib/check_mk_agent/local/600/  


## Example
Here is an example of how the checks look in checkmk:


![Example](/freebsd.png)


# License 
This project is licensed under the MIT license. See the [LICENSE](LICENSE) for details.
