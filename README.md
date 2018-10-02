# Moz' Cookbook

Notes:
 - Remote host: javiersl.com
 - Remote user: moz
 - Local user: woz

## Network

### Telnet to a port
    telnet -l moz javiersl.com:8080

### Test TCP connection
    echo > /dev/tcp/javiersl.com/8080 && echo "Connection established" || echo "Can't connect to remote host"

### Test UDP connection
    echo > /dev/udp/javiersl.com/67 && echo "Connection established" || echo "Cant'connect to remote host"

## Files & Directories

### Copy the file "foo.txt" from remote host to local
    scp moz@javiersl.com:/home/moz/foo.txt /home/woz

### Copy the file "foo.txt" from local to a remote host
    scp /home/woz/foo.txt moz@javiersl.com:/home/moz

### Copy the directory "foo" from local to a remote host's directory "bar"
    scp -r /home/woz/foo moz@javiersl.com:/home/moz/bar