# 基础数据类型

## 整型(Integer)
## 浮点型

# 算术操作

* 指数操作符: `**`

```ruby
puts 2**3 # 8
```

# 对象类型

## 字符串类型(String)

*  `#{ expr } ` 字符串嵌入表达式。

```ruby
puts 'escape using "\\"'; # escape using "\"
puts 'That\'s right'; # That's right

puts "相乘 : #{24*60*60}"; # 相乘 : 86400

name1 = "Joe"
name2 = "Mary"
puts "你好 #{name1},  #{name2} 在哪?" # 你好 Joe,  Mary 在哪?
``` 

* 字符串内建

```rb
#!/usr/bin/ruby -w
# -*- coding: UTF-8 -*-

myStr = String.new("THIS IS TEST")
foo = myStr.downcase
puts "#{foo}" # this is test
```

## 数组（Array）

```rb
#!/usr/bin/ruby -w
# -*- coding: UTF-8 -*-

arr1 = Array.new
arr2 = Array.new(20) # 设置数组的大小
arr3 = Array.new(4, "mac") # ["mac", "mac", "mac", "mac"]
arr4 = Array.new(10) { |e| e = e * 2 } # [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
arr5 = Array.[](1, 2, 3, 4,5) # [1, 2, 3, 4, 5]
arr6 = Array[1, 2, 3, 4,5] # [1, 2, 3, 4, 5]
arr7 = Array(0..9) # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

# 数组的大小
puts arr2.size  # 返回 20
puts arr2.length # 返回 20

# 获取数组值
index1 = arr7.at(6) # 6
```

* [数组常用方法](https://www.runoob.com/ruby/ruby-array.html)

## 哈希（Hash）

```rb
#!/usr/bin/ruby -w
# -*- coding: UTF-8 -*-

# 创建哈希
hash1 = Hash.new
hash2 = Hash.new( "month" )
hash3 = {"1" => "January", "2" => "February"}

# 哈希的大小
size = hash3.size
```

## 范围（Range）

```rb
(1..5)        #==> 1, 2, 3, 4, 5
(1...5)       #==> 1, 2, 3, 4
('a'..'d')    #==> 'a', 'b', 'c', 'd'
```

## 日期 & 时间（Date & Time）

# 迭代器

```rb
hash = {"1" => "January", "2" => "February"}
hash.keys.each do |item|
  puts item
end
```

```rb
#!/usr/bin/ruby -w
# -*- coding: UTF-8 -*-

hash3 = {"1" => 1000, "2" => 2000}

total = 0
hash3.each {|key,value| total += value }
puts total.to_s # 3000
```

# 流程控制

## 条件句

```rb
#!/usr/bin/ruby -w
# -*- coding: UTF-8 -*-

var1 = 4
var2 = 5

if var1 = var2 then
  puts "1"
elsif var1 != var2 then
  puts "2"
else
  puts "3"
end
```

## 循环

```rb
#!/usr/bin/ruby -w
# -*- coding: UTF-8 -*-

var1 = 4
var2 = 5

while var1 = var2 do
  # code
end

while var1 = var2
  # code
end
```

# 方法

* Ruby 中的 return 语句用于从 Ruby 方法中返回一个或多个值。
* Ruby 中的每个方法默认都会返回一个值。这个返回的值是最后一个语句的值。

```rb
#!/usr/bin/ruby -w
# -*- coding: UTF-8 -*-

def method_name1
  # no ret
end

# 方法带参数、参数设置默认值
def method_name2 (var1,var2="1")
  # no ret
end

# 方法调用
method_name1
method_name2 25, 30

# Ruby 中的每个方法默认都会返回一个值。这个返回的值是最后一个语句的值。
def test
  i = 100
  j = 10
  k = 0
end

ret = test
puts ret # 0
```

## 类方法

当方法定义在类的外部，方法默认标记为 private。另一方面，如果方法定义在类中的，则默认标记为 public。 

# 块

* 用`yield`语句来调用块。

```rb
#!/usr/bin/ruby -w
# -*- coding: UTF-8 -*-

def test
  puts "在 test 方法内"
  yield
  puts "你又回到了 test 方法内"
  yield
end

test {puts "你在块内"}

# 在 test 方法内
# 你在块内
# 你又回到了 test 方法内
# 你在块内
```

# 模块（Module）

* 模块（Module）是一种把方法、类和常量组合在一起的方式。
* 如果一个第三方的程序想要使用任何已定义的模块，则可以简单地使用 Ruby require 语句来加载模块文件

```rb
#!/usr/bin/ruby -w
# -*- coding: UTF-8 -*-

module Tag
  var1 = 1
  def func_name1
  end

  class Cls1
    def func_name2
    end
  end
end
```

































