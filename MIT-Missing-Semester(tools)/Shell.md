# 基本指令
## $PATH
存储Shell运行程序地址
## pwd
Print Working Directory
## cd
Change directory
- .: 当前目录
- .. : 父目录
- ~ : 根目录
- - : 上一个目录
## ls
List the files
- r: 可读
- w: 可写
- x: 可执行
## mv
可移动可重命名
## <>
- ">"表示输出
- "<"表示输入
> echo hello > hello.txt
- ">>" 表示追加
## |
通道符
左侧的输出作为右侧的输入
## sudo
以管理员（superadmin）执行
## =
赋值？ 对空格非常敏感 前后都不应有空格
## “ ‘
双引号会执行内部符号如（￥#！） 单引号不会
## $
- `$0` - 脚本名
- `$1` 到 `$9` - 脚本的参数。 `$1` 是第一个参数，依此类推。
- `$@` - 所有参数
- `$#` - 参数个数
- `$?` - 前一个命令的返回值
- `$$` - 当前脚本的进程识别码
- `!!` - 完整的上一条命令，包括参数。常见应用：当你因为权限不足执行命令失败时，可以使用 `sudo !!` 再尝试一次。
- `$_` - 上一条命令的最后一个参数。如果你正在使用的是交互式 shell，你可以通过按下 `Esc` 之后键入 . 来获取这个值。