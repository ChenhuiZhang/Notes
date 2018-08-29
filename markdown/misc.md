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
