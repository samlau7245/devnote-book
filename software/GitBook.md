# 本地服务部署

```sh
# 安装GitBook，终端输入
brew install gitbook-cli -g

# 创建书本文件夹，初始化文件目录
gitbook init

# 预览效果
gitbook serve

# 编译
gitbook build
```

# 插件

## Disqus 评论

```json
"plugins": [
    "disqus"
],
"pluginsConfig": {
    "disqus": {
        "shortName": "gitbookuse"
    }
}
```

## Search Plus

```json
{
    "plugins": ["-lunr", "-search", "search-plus"]
}
```

## Alerts

```shell
> **[info] For info**
>
> Use this for infomation messages.

> **[warning] For warning**
>
> Use this for warning messages.

> **[danger] For danger**
>
> Use this for danger messages.

> **[success] For info**
>
> Use this for success messages.
```

# 资料

* [GitBook](https://chrisniael.gitbooks.io/gitbook-documentation/content/index.html)
