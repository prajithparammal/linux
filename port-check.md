#### nc command
```
nc -vl 1600 > Doubletake (receiving end)
nc -v -v -l -p 2222 >/dev/null
nc 10.95.22.143 1600 < /var/tmp/DoubleTake-8.1.1.1013.2-1.x86_64.rpm (from where file is transferring; source)
```

#### Multiple Ports checking on list of servers in a file. Here srv.txt
```
for i in `cat srv.txt` ; do echo -e "111\n6320\n6325\n6326\n443\n1500\n1501\n1505\n1506" | xargs -i nc -w 3 -zv $i {}; done
```
