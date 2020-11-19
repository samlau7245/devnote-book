
> 遍历文件的每行，把符合条件的行内容输出。

```sh
#!/bin/bash

FILEPATH='/Users/shanliu/Desktop/aa.txt'
CONTAINSTR='title='
list=(1,2)
cat $FILEPATH | while read line
do
	LINE=${line}
	if [[ $LINE == *$CONTAINSTR* ]]; then
		echo $LINE
	fi
done >> b.txt
```

--- 

> `2>/dev/null`

Linux系统预留可三个文件描述符:

* 1 : 标准输入(stdin)
* 2 : 标准输出(stdout)
* 3 : 标准错误(stderr)

```sh
$> shell_dir % ls
123.txt
$> shell_dir % ls 123.txt 
123.txt
$> shell_dir % ls 456.txt
ls: 456.txt: No such file or directory
```

`/dev/null` 是一个特殊的设备文件，这个文件接收到任何数据都会被丢弃。因此，`null`这个设备通常也被称为位桶（bit bucket）或黑洞。所以，`2>/dev/null`的意思就是将标准错误stderr删掉。

---

> 重定向

* `>` 会先清空文件，再写入文件。
* `>>` 将内容追加到现有文件的尾部。

---

* `$0` 当前脚本的文件名
* `$?` 上个命令的退出状态，或函数的返回值。
* `$0` 传递给脚本或函数的参数。n 是一个数字，表示第几个参数。例如，第一个参数是$1，第二个参数是$2。
* `$0` 


# 关系运算符

| 运算符 | 说明 | 举例 |
| -- | -- | -- |
|-ne| 检测两个数是否不相等，不相等返回 true。 | [ $a -ne $b ] 返回 true。 |
| -eq | 检测两个数是否相等，相等返回 true。| [ $a -eq $b ] 返回 false。|













