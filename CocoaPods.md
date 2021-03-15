
# 命令行

## Specifications

### [pod spec lint](https://guides.cocoapods.org/terminal/commands.html#pod_spec_lint) 远程仓库校验

## Libraries

### pod lib create

```sh
pod lib create NAME
```

创建一个名为`NAME`的 Pod 脚手架。

* `--template-url=URL`: The URL of the git repo containing a compatible template.


### pod lib lint

[pod lib lint](https://guides.cocoapods.org/terminal/commands.html#pod_lib_lint)

```sh
pod lib lint [PODSPEC_PATHS ...]
```

使用工作目录中的文件验证Pod。

* `--allow-warnings`: 忽略警告。
* `--subspec=NAME`: 校验 subspec。
* `--no-subspecs`: 跳过校验 subspec。
* `--use-libraries`: Lint uses static libraries to install the spec. 使用到第三方库。
* `--include-podspecs=**/*.podspec`: Additional ancillary podspecs which are used for linting via :path.

```
s.default_subspec = 'Core'
```

```sh
pod lib lint \
--allow-warnings \
--use-libraries \
--verbose \
--include-podspecs=/Users/shanliu/Desktop/UhomeModules/git_path/寻常生活/5.3.0/commonmediator/ \
--sources='https://github.com/CocoaPods/Specs.git,http://gitlab.uhomecp.com:9200/jingjie/segpodrepo.git' \
```

* [CocoaPods Command-line Reference](https://guides.cocoapods.org/terminal/commands.html#commands)
* [CocoaPods进阶：详解私有库制作](https://juejin.cn/post/6844903665258463239)

```sh
# pod package Commom.podspec --force --embedded --no-mangle --exclude-deps --subspecs='SEGInterfaceManager' --spec-sources='https://gitee.com/samcoding/SMSpecs.git,https://github.com/CocoaPods/Specs'
# pod package Commom.podspec --force --embedded --no-mangle --exclude-deps --subspecs='SEGWeb' --spec-sources='https://gitee.com/samcoding/SMSpecs.git,https://github.com/CocoaPods/Specs'

# pod package Commom.podspec --force --embedded --no-mangle --exclude-deps --subspecs='SEGServerManager'
# pod package Commom.podspec --force --embedded --no-mangle --exclude-deps --subspecs='SEGInterfaceManager'
# pod package Commom.podspec --force --embedded --no-mangle --exclude-deps --subspecs='SEGInterfaceManager/SEGLoginSource'
# pod package Commom.podspec --force --embedded --no-mangle --exclude-deps  --subspecs='SEGWeb'
# pod package Commom.podspec --force --embedded --no-mangle --exclude-deps --subspecs='SEGMediator'
# pod package Commom.podspec --force --embedded --no-mangle --exclude-deps --subspecs='SEGMediator,SEGPlatform,SEGColor'
# pod package Commom.podspec --force --embedded --no-mangle --exclude-deps --subspecs='SEGMediator,SEGPlatform,SEGColor,SEGLayoutMacro'
# pod package Commom.podspec --force --embedded --no-mangle --exclude-deps --subspecs='SEGMediator,SEGPlatform,SEGColor,SEGLayoutMacro,SEGTools/SEGCKeyChainStore'
# pod package Commom.podspec --force --embedded --no-mangle --exclude-deps --subspecs='SEGMediator,SEGPlatform,SEGColor,SEGLayoutMacro,SEGTools/SEGCKeyChainStore,SEGTools/YYBase,SEGTools/SEGModel'
# pod package Commom.podspec --force --embedded --no-mangle --exclude-deps --subspecs='SEGMediator,SEGPlatform,SEGColor,SEGLayoutMacro,SEGTools/SEGCKeyChainStore,SEGTools/YYBase,SEGTools/SEGModel,SEGServerManager,SEGInterfaceManager/SEGLoginSource,SEGInterfaceManager/SEGProfileSource,SEGInterfaceManager/SEGMultipartfileuploadSource'
# pod package Commom.podspec --force --embedded --no-mangle --exclude-deps  --subspecs='SEGPhotoLibrary'


# cd /Users/shanliu/Desktop/MediatorCreate/Common/trunk/
# pod lib lint --allow-warnings --verbose
# pod repo push SMSpecs Commom.podspec --allow-warnings
# pod repo-svn push SVNSpecs Commom.podspec





# pod spec lint --sources='https://github.com/CocoaPods/Specs.git,http://gitlab.uhomecp.com:9200/jingjie/segpodrepo.git' --no-clean --verbose --skip-import-validation --fail-fast --use-libraries  --use-libraries --allow-warnings
# pod repo push segrepo  SEGCommunitySocial.podspec --allow-warnings --use-libraries --sources='https://github.com/CocoaPods/Specs.git,http://gitlab.uhomecp.com:9200/jingjie/segpodrepo.git' --skip-tests --verbose --skip-import-validation  
```
