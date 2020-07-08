# 初始化

```sh
my_array=(A B "C" D)
# 定义一个数组类型的变量
declare -a list;
```
# 读取数组

```sh
${array_name[index]}
```

# 数组中的所有元素

```sh
echo "数组的元素为: ${my_array[*]}"
echo "数组的元素为: ${my_array[@]}"
```

# 数组的长度

```sh
echo "数组元素个数为: ${#my_array[*]}"
echo "数组元素个数为: ${#my_array[@]}"
```

# 删除

```sh
# 使用 unset 关键字来删除数组元素
unset array_name[index]
# 删除整个数组
unset array_name
```

# 追加元素

```sh
declare -a list;
for i in `ls`; do
	list[${#list[*]}]=$i;
done
```