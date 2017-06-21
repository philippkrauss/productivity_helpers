# productivity_helpers

The following list of commands help me in my day to day work, but I don't need them often enough to remember them...

### serialize a groovy xml object to string
groovy.xml.XmlUtil.serialize(xml)

### CIFS mount on linux
mount -t cifs -o username=domain\\\\user "//host/share" /mnt

### targz/untargz
tar czvf file.tar.gz directory
tar xvfz file.tar.gz

### ls sorted by file modification time
ls -lt[r]

### add user to sudo
visudo -> `username` ALL=(ALL) NOPASSWD: ALL

### bad interpreter problem (unix/windows line endings)
/bin/sh^M: bad interpreter: No such file or directory ->

vi, :set fileformat=unix, :wq!

### show open port
sudo netstat -tulpn

### openssl handshake
openssl s_client -connect localhost:9443

python script for ssl connection check: [cipherscan](https://github.com/mozilla/cipherscan)

### tcpdump
tcpdump -ni any -s 0 -w - port 9444

### login without password
#!/usr/bin/expect
spawn  ssh -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no opsa@[lrange $argv 0 1]
expect "assword:"
send "... enter password here...";
interact
