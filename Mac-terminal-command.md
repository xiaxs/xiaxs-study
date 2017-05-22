/*
 * @author: xiaxs(xxs19910202@vip.qq.com)
*/

1. Mac 文件目录
    " / "   --> 根目录 --> cd /
    " ~ "   --> 用户主目录的缩写,如: 当前用户为zsh,那么 "~" 展开就是 /Users/zsh --> cd ~
    " . "   --> 当前目录 --> cd .
    " .. "  --> 父级目录(上级目录) --> cd ..

2. cd 跳转到某个目录(输入目录时只要按下tab键可以自动补全)
    cd /Users/zsh/Desktop

3. ls
    列出当前目录下的子目录和文件

4. pwd 显示当前目录的路径
    example: cd /users/zsh  --> pwd --> /users/zsh

5. clear 清空当前输入
    如果Terminal窗口中的内容太多了，可以用clear命令将其清空

6. history 查看输入历史记录
    在Terminal输入命令时,可以使用上下方向键查看之前输入的命令,另外,可以用history查看输入的完整历史

7. mkdir 创建一个目录
    mkdir <dirname>

8. rmdir 删除一个目录
    rmdir <dirname>

9. mvdir 移动或者重命名一个目录
    mvdir dir1 dir2

10. dircmp 比较两个目录的内容
    dircmp dir1 dir2

11. touch 更新文件的访问和修改时间
    touch -m 05202400 filename

12. alias 给某个命令定义别名
    alias del=em -i

13 unalias 取消对某个别名的定义
    unalias del

14 who 列出当前登录的所有用户
    who

15 env 显示当前所有设置过的环境变量
    env

16 whoami 显示当前正在操作的用户名
    whoami

17 tty 显示终端或伪终端的名称
    tty
