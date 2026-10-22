# PickAbc

<a href="https://github.com/joseygo/PickAbc/releases/latest">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/badge-download-dark.svg">
    <img src="assets/badge-download.svg" alt="下载 PickAbc · Windows 10/11" height="30">
  </picture>
</a>

**简体中文** · [English](README.en.md)

一个常驻置顶的文本面板：把常用的话存起来，点一下就能复制粘贴，也可以直接拖到任意输入框。

![PickAbc](design/pickabc-ui.png)

## 下载即用（Windows 10 / 11）

到 [Releases](https://github.com/joseygo/PickAbc/releases) 下载 `PickAbc-1.0.1-win64.zip`，解压后双击 `PickAbc.exe`。
无需安装 Python，无需联网，无第三方依赖，单文件约 9.5 MB。

## 怎么用

| 操作 | 效果 |
|---|---|
| 单击文本 | 复制到剪贴板 |
| 按住文本拖出去 | 拖到任意应用的输入框松手，直接粘贴进去 |
| 从别处拖文本进来 | 拖到面板任意位置松手，弹出「添加文本」并预填内容 |
| 右键文本 | 菜单：编辑 |
| 在任意应用输入 111~999 | 弹出确认条，回车确认：抹掉数字，复制对应序号文本并粘贴（全局快捷输入） |
| 右下角 ＋ | 新增文本 |
| 编辑窗口内「删除」 | 删除该文本 |
| 右上角排序图标 | 按使用频率重新排序 |

窗口默认置顶、停靠屏幕左侧，宽度固定为屏幕的 1/4，可上下拉伸。程序为单实例：已打开时再次双击，会把原窗口提到前面。

## 数据存放

用户数据固定放在 `%APPDATA%\PickAbc`，程序更新不会丢失：

```
%APPDATA%\PickAbc\snippets.json    # 文本
```

**便携模式**：在 `PickAbc.exe` 同目录放一个空文件 `portable.flag`，数据就改存到 exe 旁边。

## 功能说明

- **首次启动**：内置 4 条示例文本；用户全部删光后不会自动复原
- **全局快捷输入**：任何应用里连敲三位相同数字（111~999）即可调用对应序号的文本
- **拖拽互通**：面板里的文本能拖到别的应用，别的应用里选中的文本也能拖进来

## 关于 iOS

本程序基于 Python + Tkinter 桌面框架，**无法打包成 iOS 应用**：iOS 不允许运行 Python
解释器，且要求原生 UIKit 应用。iPhone / iPad 上无法运行。

手机上可用系统自带的「文本替换」（设置 → 通用 → 键盘 → 文本替换）实现类似效果。

## 系统要求

- Windows 10 / Windows 11（64 位）
- 无需管理员权限，不写注册表，无后台服务

## 已知提示

首次运行 Windows 可能弹出 SmartScreen「已保护你的电脑」—— 这是未购买代码签名证书
（每年数千元）的正常现象。点「更多信息」→「仍要运行」即可。

## 版权与许可

PickAbc 为**闭源软件**，本仓库仅发布预编译的 Windows 可执行程序与使用说明；
不提供源码，不接受源码分发或再分发授权。

© 2026 Josey。保留所有权利。
