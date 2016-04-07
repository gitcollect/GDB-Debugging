# GDB 调试
------
###0. linux系统加载glibc debugging symbols进行调试
> * debuginfo-install glibc*
> * gdb somebin
> * set verbose on
> * show debug-file-directory

设置verbose，查看gdb是否读取libc.so.6的符号信息。

使用系统包管理工具安装的符号信息so默认路径是 /usr/lib/debug/lib64，查询方式：
> * rpm -ql glibc-debuginfo.x86_64 0:2.17-106.el7_2.4|grep libc.so

相关链接
  [https://sourceware.org/gdb/onlinedocs/gdb/Separate-Debug-Files.html](https://sourceware.org/gdb/onlinedocs/gdb/Separate-Debug-Files.html)
  [http://stackoverflow.com/questions/10000335/how-to-use-debug-version-of-libc](http://stackoverflow.com/questions/10000335/how-to-use-debug-version-of-libc)
