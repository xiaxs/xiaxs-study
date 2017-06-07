### tree -- 生成文件目录树

#### 1. Install Homebrew
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

#### 2. Install tree
```
brew install tree
```


#### 3. Mac下 tree命令
```
显示某个项目下3层的所有文件结构，同时又过滤node_modules文件夹，最后输出到 tree.md

tree -L 3 -I "node_modules" > tree.md
```
> tree.md会生成在当前目录

```
1. tree  -a 显示所有文件和目录

2. tree -d 显示目录名称而非内容

3. tree -f 在每个文件或目录之前，显示完整的相对路径名称

4. tree -F 在执行文件，目录，Socket，符号连接，管道名称名称，各自加上"*","/","=","@","|"号。

5. tree -r 以相反次序排列

6. tree -t 用文件和目录的更改时间排序

7. tree -L n 只显示 n 层目录 （n 为数字）

8. tree -dirsfirst 目录显示在前,文件显示在后

9. 可以加的参数
    -A 使用ASNI绘图字符显示树状图而非以ASCII字符组合。
    -C 在文件和目录清单加上色彩，便于区分各种类型。
    -D 列出文件或目录的更改时间。
    -g 列出文件或目录的所属群组名称，没有对应的名称时，则显示群组识别码。
    -i 不以阶梯状列出文件或目录名称。
    -I 不显示符合范本样式的文件或目录名称。
    -l 如遇到性质为符号连接的目录，直接列出该连接所指向的原始目录。
    -n 不在文件和目录清单加上色彩。
    -N 直接列出文件和目录名称，包括控制字符。
    -p 列出权限标示。
    -P 只显示符合范本样式的文件或目录名称。
    -q 用"?"号取代控制字符，列出文件和目录名称。
    -s 列出文件或目录大小。
    -u 列出文件或目录的拥有者名称，没有对应的名称时，则显示用户识别码。
    -x 将范围局限在现行的文件系统中，若指定目录下的某些子目录，其存放于另一个文件系统上，则将该子目录予以排除在寻找范围外。
```
转载自[博客](http://blog.csdn.net/askbai666888/article/details/9995837)
