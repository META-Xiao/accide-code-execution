# ACC-IDE 运行后端

本人先尝试用alpine和proot构建一个安卓arm架构、并集成了基本的cpp工具链和python的mini Linux运行环境，用于本地编译和运行代码。但由于安卓10后的权限收紧（对于一些手机厂商的系统限权更加收紧），尽管尝试在/data/local/tmp运行proot但还是没有权限。在我暂时没找到其他本地运行的方法前，先使用GitHub的Actions来运行后端吧😋。

>  或许还可以尝试构建针对不同cpu架构的cpp工具链，然后再构建一个.so库用于编译和运行cpp程序😾

## 食用方法

1. fork本仓库
2. 在GitHub的用户设置中，找到 `Developer Settings` -> `Personal access tokens` -> `Generate new token` -> `Generate new token (classic) ` -> 勾选 `repo`和`workflow` -> `Generate token` -> 复制保存生成的token
3. 把你fork的仓库地址和生成的token填入ACCIDE的 `设置` 中

## 注意事项

- 本项目使用GitHub Actions来运行后端，GitHub Actions对免费的个人账户有每月2000分钟的免费运行时间，所以如果运行时间过长可能会被暂停，请尽量减少运行时间。
- 如果发现了bug或者有更好的建议，欢迎提交issue或者pull request🤗。