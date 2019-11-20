##### rysnc commands:
```
rsync  -avznh --checksum --progress  root@BEZVSAPD0127:/admin  /  
rsync  -avznh --checksum --progress  root@BEZVSAPD0127:/oem  /  
rsync  -avznh --checksum --progress  root@BEZVSAPD0127:/oracle /  
rsync  -avznh --checksum --progress  root@BEZVSAPD0127:/oravrtxr/arch /oravrtxr/  
```

##### List number of folder and files under a mount point:
```
for i in `df -PH | grep ora | awk '{print $6}'`; do echo "#######Total number of files and folder under mount point $i #######"; find $i -type d -printf "d\n" -o -type f -printf "f\n" | awk '/f/{f++}/d/{d++}END{printf "%d directories, %d files\n", d, f}' ; done
```
