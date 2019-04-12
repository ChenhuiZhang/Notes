# 如何找出一个文件的归属包?
要查找出包含文件 foo 的软件包, 执行:
```
dpkg --search filename
```
在已安装软件包中搜寻 filename.(等同于搜索 /var/lib/dpkg/info/ 目录下扩展名为 .list 的文件, 并输出所有包含此文件的软件包名和版本号).

```
zgrep foo Contents-ARCH.gz
```
通过绝对路径来搜寻含 foo 字符串的文件, Contents-ARCH.gz 文件(ARCH 指要查询的平台)在 Debian FTP 的主软件包目录(main, non-free, contrib)下, 一个 Contents 文件只包含同一目录下的软件包,因此用户查找含 foo 文件的软件包，需要搜寻多个 Contents 文件.

相对于 dpkg --search 这种方法的优点是，它不仅仅搜寻系统已安装软件包.

# Save the creadential for git push
[link](https://help.github.com/categories/managing-remotes/)
Store always
```
git config --global credential.helper store
```

Set the cache to timeout after 1 hour (setting is in seconds)
```
git config --global credential.helper 'cache --timeout=3600'
```

# make plt.show() work
代码配置backend的方法：
**在import matplotlib.pyplot之前**

import matplotlibmatplotlib.use('TkAgg')  # 'TkAgg' 是我Windows上的配置，需根据自己情况修改backend是在配置文件中配置的

得到配置文件路径的方法
import matplotlibprint
matplotlib.matplotlib_fname()

查询backend的方法：

matplotlib.get_backend()

或

matplotlib.pyplot.get_backend()

# Wildcard filter in Wireshark
**eth.src[0:3] == 00:20:4a**

# Change the git repo url from git://* to https://*
```
git config --global url.https://github.com/.insteadOf git://github.com/
```

# Systemd-analyze
```
# systemd-analyze blame
# systemd-analyze critical-chain
# systemd-analyze plot > boot_analysis.svg
# systemd-analyze blame -H root@192.168.77.5
# systemd-analyze critical-chain -H root@192.168.77.5
# man systemd-analyze
```

# kmemleak

```
CONFIG_HAVE_DEBUG_KMEMLEAK=y
CONFIG_DEBUG_KMEMLEAK=y
CONFIG_DEBUG_KMEMLEAK_EARLY_LOG_SIZE=8000
# CONFIG_DEBUG_KMEMLEAK_TEST is not set
# CONFIG_DEBUG_KMEMLEAK_DEFAULT_OFF is not set
CONFIG_DEBUG_KMEMLEAK_WARN=y
```
[link](https://www.kernel.org/doc/html/latest/dev-tools/kmemleak.html)

# scp in ipv6
scp lg@\[2101:da8:a000:12:bc26:9915:4b1d:64cc\]:/home/lg/example.c ~/home/lg/src

# Take screenshot in Mplayer

Enable screenshot filter
When we want to take screenshots when playing video, first we need to set the “-vf screenshot” option:

```
$ mplayer -vf screenshot video.file
```

If we want to enable the screenshot filter by default, we may put the option by adding one line into ~/.mplayer/config :

```
vf=screenshot
```

To take a single screenshot
Just press ‘s‘.

To take continuous screenshots
To start taking continuous screenshots, press ‘S‘; press ‘S‘ again to stop.

Remember to stop it, otherwise mplayer will keep taking screenshots.

Screenshots will be stored under the current directory with name “shot00001.png”, “shot00002.png”, and so on.

That’s quite easy, right? Then enjoy it~

# Calculate the PI
echo "scale=10000; 4*a(1)" | bc -l  // tan(PI/4) = 1 => PI = 4*atan(1)
