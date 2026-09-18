# BiliBestAdBlock

公开仓库中的 `README.md` 用于说明模块来源与导入方法。

面向 Shadowrocket 的个人 Bilibili 净化模块。它保留已在 Bilibili 国际版验证有效的 `Search/SearchAll` Protobuf 搜索广告过滤，同时处理部分开屏、动态、评论、直播推广，并按当前个人偏好隐藏搜索发现、精简“我的”页面。

模块文件：[BiliBestAdBlock.sgmodule](./BiliBestAdBlock.sgmodule)

## Shadowrocket 导入

复制此模块的原始文件 URL：

```text
https://raw.githubusercontent.com/Enderherman/BiliBestAdBlock/main/BiliBestAdBlock.sgmodule
```

在 iPhone 上打开 **Shadowrocket → 配置 → 模块 → 右上角“+”**，粘贴 URL 并下载，确认模块前有勾选。当前配置需开启 HTTPS 解密、安装并完全信任证书，并开启“通过 HTTP/2 进行中间人攻击（MitM）”。随后重新连接 Shadowrocket，彻底退出 Bilibili 再启动。

启用此模块时，关闭原来的 `Bilibili增强`、`BiliIntlClean` 与 All-in-One-AdBlock 的 Bilibili 部分，以免多个脚本修改同一个响应。`All-in-One-Other-Apps` 可继续用于其他 App，AWAvenue 广告规则也可保留。

用原来会出现搜索广告的关键词复测，并检查首页、动态、评论、直播和“我的”页是否正常。若出现异常，先只关闭本模块复测，再记录具体页面、App 版本及 Shadowrocket 脚本日志。规则会随 Bilibili 接口变化而失效；仓库文件能在线更新，但手机端是否自动刷新取决于 Shadowrocket 的模块更新设置。

## 参考与致谢

本模块是为个人使用整理的合并配置，参考或改写了以下公开规则；不是这些项目的官方版本：

- [Bilibili增强](https://github.com/lushier888/QX-Surge-Loon-Shadowrocket/blob/main/SurgeModule/BilibiliAD.sgmodule)：主要规则与 Sparkle 脚本调用方式。
- [BiliIntlClean](https://github.com/iab0x00/ProxyRules/blob/main/Rewrite/BiliIntlClean.sgmodule)：搜索发现和“我的”页精简思路。
- [All-in-One-AdBlock](https://github.com/letswish/Shadowrocket-Module/blob/main/All-in-One-AdBlock.sgmodule)：补充不重叠的 Bilibili 广告域名与接口规则。
- [Sparkle](https://github.com/kokoryh/Sparkle)：Protobuf 与 JSON 响应处理脚本；脚本仍由上游地址加载。Sparkle 仓库标注为 [GPL-3.0](https://github.com/kokoryh/Sparkle/blob/master/LICENSE)。
- [R-Store](https://github.com/zirawell/R-Store)：观影页响应处理脚本；脚本仍由上游地址加载。

这些上游脚本由原作者维护；本仓库未包含其脚本源码。规则组合与“我的”页的独占处理逻辑为本地调整。请以各上游仓库的声明为准。
