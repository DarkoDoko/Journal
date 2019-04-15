### 2019-04-03

Problem: sum all longs from a map

Solution:

`long total = mapName.values().stream().reduce(0L, Long::sum);`


### 2019-04-12

Problem: dump thread info in log

Solution:
0) find pid of process in question
1) top -H shows resource utilization per thread instead of per process, note the thread id
2) send kill -3 signal to pid from step 0)
3) application log now contains full thread dump.  Every thread info starts with line
  `"main" #1 prio=5 os_prio=0 tid=0x00007f4978011000 nid=0x685c` where nid=0x... contains thread id (the one taken from step 1) in hex format
