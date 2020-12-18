
# 规则

格式：

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<break changes>
<affect issues>
```

示例：

```
build(A.json): 修改了A的依赖版本

为了支持B修改了A的版本。

BREAKING CHANGE:CCCC。
```

## type 

> type 必填项，用于指定commit的类型。

* `feat`: 增加新功能。
* `fix`: 修复bug。
* `docs`: 只改动了文档相关的内容。
* `style`: 不影响代码含义的改动，例如去掉空格、改变缩进、增删分号。
* `build`: 构造工具的或者外部依赖的改动，例如webpack，npm。
* `refactor`: 代码重构时使用。
* `revert`: 执行`git revert`打印的message。
* `test`: 添加测试或者修改现有测试。
* `perf`: 提高性能的改动。
* `ci`: 与CI（持续集成服务）有关的改动。
* `chore`: 不修改src或者test的其余修改，例如构建过程或辅助工具的变动。
* `release`: 发布版本提交

## scope

> 必填项，用于描述改动的范围，格式为项目名/模块名。如果一次commit修改多个模块，建议拆分成多次commit，以便更好追踪和维护。

## subject

> 精简的描述。

## body

> 填写详细描述，主要描述`改动之前的情况`及`修改动机`，对于小的修改不作要求，但是重大需求、更新等必须添加body来作说明。

## break changes

> 指明是否产生了破坏性修改，涉及break changes的改动必须指明该项，类似版本升级、接口参数减少、接口删除、迁移等。

## affect issues

> 指明是否影响了某个问题。