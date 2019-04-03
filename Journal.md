### 2019-04-03

Problem: sum all longs from a map

Solution:

`long total = mapName.values().stream().reduce(0L, Long::sum);`
