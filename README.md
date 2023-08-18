# 简介
将shellcode注入到已经存在的RWX内存中，避免了申请内存修改内存的高危操作
基于SysWhispers3使用syscall的方式打开进程和远程调用shellcode

# 分段注入
直接将shellcode注入容易被yara规则匹配，而将shellcode随机分段注入其他进程则可以规避这一规则

# 微步
![image](https://github.com/ToT0vO/RWX_loader/assets/129960499/0b691abf-7705-4717-b359-243d9ad554b4)
>https://s.threatbook.com/report/file/8a2dfca748c593c46d902cb27fa5c8fe19450a88d27929dc1a7c3e315b4081f6

# 微步特征匹配情况
![3QO{5_@~D(YTLQWRL~Y L G](https://github.com/ToT0vO/RWX_loader/assets/129960499/ae61dd54-e65c-46f3-979b-05fa9e3107fa)
可以发现识别到了内存写入，但是并没有识别为恶意shellcode

# 效果
![AE)2JZG_H QMP6ZATNHTQII](https://github.com/ToT0vO/RWX_loader/assets/129960499/2eac23d9-de94-46db-834c-38a5b4acba89)
