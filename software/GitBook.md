# 本地服务部署

```sh
# 安装GitBook，终端输入
npm install gitbook-cli -g

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

# 错误

```
TypeError: cb.apply is not a function
    at /opt/homebrew/lib/node_modules/gitbook-cli/node_modules/npm/node_modules/graceful-fs/polyfills.js:287:18
```

[解决](https://stackoverflow.com/questions/64211386/gitbook-cli-install-error-typeerror-cb-apply-is-not-a-function-inside-graceful)

```
cd /opt/homebrew/lib/node_modules/gitbook-cli/node_modules/npm/node_modules/
npm install graceful-fs@latest --save
```