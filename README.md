# terminal commands

type|command
:-:|:-:
search|[find](#001-find)
<hr/>

## 001 find
- show files modified as of 8am today, print only date time and filename
 ```bash
 find . -not -path "*/.*" -type f -newermt "$(date +%Y-%m-%d) 08:00" -ls | awk '{print $8, $9, $10, $11}'
 ```
<hr/>

