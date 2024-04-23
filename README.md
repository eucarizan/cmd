# terminal commands

type|command
:-:|:-:
search|[find](#001-find)
copy|[find exec](#002-find-exec)
<hr/>

## 001 find
- show files modified as of 8am today, print only date time and filename
 ```bash
 find . -not -path "*/.*" -type f -newermt "$(date +%Y-%m-%d) 08:00" -ls | awk '{print $8, $9, $10, $11}'
 ```
<hr/>

## 002 find exec
- find files modified since $arg1 (time) today and copy to $arg2 directory
 ```bash
 find . -not -path "*/.*" -type f -newermt "$(date +%Y-%m-%d) $1" -exec cp {} $2 \;
 ```
<hr/>

<!--

## 000 a
- a
 ```bash
 :r !tail -n1 /path/to/file
 ```
<hr/>
-->
