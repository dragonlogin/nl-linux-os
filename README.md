(1)汇编级调试
 确认在 oslab 目录下
 
$ cd ~/oslab/

运行脚本前确定已经关闭刚刚运行的 Bochs

$ ./dbg-asm

（2）C 语言级调试

$ cd ~/oslab
$ ./dbg-c

$ cd ~/oslab
$ ./rungdb

oslab 下的 hdc-0.11-new.img 是 0.11 内核启动后的根文件系统镜像文件，相当于在 bochs 虚拟机里装载的硬盘。在 Ubuntu 上访问其内容的方法是：

$ cd ~/oslab/


启动挂载脚本

$ sudo ./mount-hdc

之后，hdc 目录下就是和 0.11 内核一模一样的文件系统了，可以读写任何文件（可能有些文件要用 sudo 才能访问）。
进入挂载到 Ubuntu 上的目录

$ cd ~/oslab/hdc

查看内容

$ ls -al

读写完毕，不要忘了卸载这个文件系统：
$ cd ~/oslab/

卸载

$ sudo umount hdc