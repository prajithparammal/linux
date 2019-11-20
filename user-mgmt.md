#### Set user password to never expire
```
passwd -x -1  username
chage -I -1 -m 0 -M 99999 -E -1 username
```

