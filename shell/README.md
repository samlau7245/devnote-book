
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