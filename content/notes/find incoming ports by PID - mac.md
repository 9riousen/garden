---
title: "PID를 알고있을때 열린 port 목록 찾기 (MacOS)"
date: '2023-06-26'
images: ['https://images.idgesg.net/images/article/2020/01/nwht_050_lsof-100826152-orig.jpg']
---
![lsof](https://images.idgesg.net/images/article/2020/01/nwht_050_lsof-100826152-orig.jpg)

port를 사용하는 process를 찾고 싶은게 아니다. PID로 port목록 찾기

```bash
% lsof -Pan -p 94880 -i
COMMAND   PID USER   FD   TYPE             DEVICE SIZE/OFF NODE NAME
Box     94880 user   29u  IPv4 0xe45f74d3595521e5      0t0  TCP 192.168.75.176:49709->104.18.34.223:443 (CLOSE_WAIT)
Box     94880 user   31u  IPv4 0xe45f74d358e7d6d5      0t0  TCP 192.168.75.176:49711->74.112.186.144:443 (CLOSE_WAIT)
Box     94880 user   32u  IPv4 0xe45f74d35784c0b5      0t0  TCP 192.168.75.176:49712->74.112.186.144:443 (CLOSE_WAIT)
Box     94880 user   33u  IPv4 0xe45f74d3573675a5      0t0  TCP 192.168.75.176:63246->104.18.34.223:443 (CLOSE_WAIT)
Box     94880 user   34u  IPv4 0xe45f74d3573796d5      0t0  TCP 192.168.75.176:63621->74.112.186.144:443 (ESTABLISHED)
Box     94880 user   35u  IPv4 0xe45f74d3579c8e25      0t0  TCP 192.168.75.176:63643->74.112.186.146:443 (ESTABLISHED)
Box     94880 user   38u  IPv4 0xe45f74d35784e1e5      0t0  TCP 192.168.75.176:63625->74.112.186.144:443 (ESTABLISHED)
```

---
- [[tags/macOS|macOS]]
- [List ports a process PID is listening on (preferably using iproute2 tools)? | StackExchange](https://unix.stackexchange.com/a/157824/53052)
