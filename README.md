# daemon

## 守护进程
```
 可为web服务在意外中断时自动重启
 实现思路：
   1.启用一个进程，将web服务的启动命令行 作为参数 启动一个子进程
   2.监听子进程的运行状态
   2.子进程退出通过chan 通知父进程 进行重启（重新执行web服务的启动命令）
```

## 使用方法
