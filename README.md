# boot_p_c

进入该目录，然后执行以下命令

```
python start_p_c.py
```

然后就在后台启动四个JVM（按照官方提供的启动参数），分别是一个Consumer和三个Provider（small、medium和large），日志不会在控制台中打印，而是会在目录中生成相应的日志文件。不过因为Provider和Consumer是固定由官方提供的，所以这些日志其实也没什么用。通过`jps`可以验证确实已经在后台启动了。

因为启动的这些JVM都是启动它的控制台的子进程，当你想关闭这些JVM时，只需要退出启动它的控制台就可以了。

内存小的电脑切记将启动参数中的xmx与xms调小一点，我这里用的是官方给的参数，非常的大，内存小的电脑可能吃不消。(官方的provider，consumer外加agent的JVM启动参数总计要占用14G内存，如果你没有那么大内存的话，一定要调小些)。
