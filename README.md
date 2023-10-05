<div align="center">
  <a href="#"><img src="https://kiramibot.dev/img/logo.svg" width="180" height="180" alt="KiramiBotPluginLogo"></a>
</div>

<div align="center">

# kirami-plugin-qweather

_✨ 基于和风天气的天气查询、订阅与推送插件 ✨_


<a href="./LICENSE">
    <img src="https://img.shields.io/github/license/FrostN0v0/kirami-plugin-qweather.svg" alt="license">
</a>
<a href="https://pypi.python.org/pypi/kirami-plugin-qweather">
    <img src="https://img.shields.io/pypi/v/kirami-plugin-qweather.svg" alt="pypi">
</a>
<img src="https://img.shields.io/badge/python-3.10+-blue.svg" alt="python">

</div>

## 📖 介绍

基于[和风天气](https://www.qweather.com/)的天气查询、订阅与推送插件

在 [nonebot-plugin-heweather](https://github.com/kexue-z/nonebot-plugin-heweather) 的基础上添加了私聊与群聊的天气订阅与推送功能

## 💿 安装

在 KiramiBot 项目的插件目录下, 打开命令行, 根据你使用的包管理器, 输入相应的安装命令

<details>
<summary>pip</summary>
  
```bash
pip install kirami-plugin-qweather
```
</details>
<details>
<summary>pdm</summary>

```bash
pdm add kirami-plugin-qweather
```
</details>
<details>
<summary>poetry</summary>

```bash
poetry add kirami-plugin-qweather
```
</details>
<details>
<summary>conda</summary>

```bash
conda install kirami-plugin-qweather
```
</details>

打开 KiramiBot 项目根目录下的配置文件, 以 `kirami.toml` 为例，在 `[plugin]` 部分追加写入
```toml
plugins = ["kiramit_plugin_qweather"]
```

## ⚙️ 配置

在 KiramiBot 项目的配置文件中添加下表中的必填配置

| 配置项 | 必填 | 默认值 | 说明 |
|:-----:|:----:|:----:|:----:|
| qweather_apikey | 是 | 无 | APIKEY |
| qweather_apitype | 是 | 无 | api 类型 |
| qweather_hourlytype | 否 | 1 | 逐小时天气返回类型：1 = 未来12小时 (默认值) 2 = 未来24小时 |

### api类型说明

0 = 普通版 免费订阅 (7 天天气预报, 1000次请求/天)

1 = 个人开发版 标准订阅 (7 天天气预报)

2 = 商业版 (7 天天气预报)

### APIKEY获取方式

**1、注册和风天气账号**  
进入官网注册[https://id.qweather.com/#/login](https://id.qweather.com/#/login)  
**2、进入控制台**  
登录后，点击 “和风天气开发者控制台”  
**3、创建项目**  
点击控制台左侧 “项目管理”，然后点击 “创建项目”，根据提示自行填写  
“选择订阅” -> “免费订阅”，“设置 KEY” -> “Web API”，都填好后“创建”  
**4、获取 key**  
返回 “项目管理”，可以看到创建的项目，点击 KEY 下面的 “查看”。

## 🎉 使用
### 指令表
| 指令 | 权限 | 需要@ | 范围 | 说明 |
|:-----:|:----:|:----:|:----:|:----:|
| 天气 | 用户 | 否 | 全部 | 查询天气，支持跟随城市名、以英文逗号分隔的经纬度 如：北京天气、120.38946,36.07223天气、天气 武汉 |
| 天气订阅 | 用户 | 否 | 全部 | 私人天气订阅，将以私聊形式推送（请确保有机器人好友），命令格式 天气订阅 [地名/经纬度] [推送时间(小时)] 如：天气订阅 北京 10。不跟随推送时间参数默认推送时间为早上8点 |
| 查询天气订阅 | 用户 | 否 | 全部 | 查询你的私人天气订阅 |
| 删除天气订阅 | 群员 | 否 | 群聊 | 按订阅id删除你的天气订阅，订阅id请先执行查询命令获取 |
| 群天气订阅 | 群员 | 否 | 群聊 | 群天气订阅，将在群聊内推送并@订阅者，命令格式同私人订阅 |
| 查询群天气订阅 | 群员 | 否 | 群聊 | 查询你在本群的天气订阅 |
| 删除群天气订阅 | 群员 | 否 | 群聊 | 按订阅id删除你在本群的天气订阅，订阅id请先执行查询命令获取 |

### 效果图

<img align="left" src="https://ghproxy.com/https://raw.githubusercontent.com/FrostN0v0/kirami-plugin-qweather/master/example1.jpg" width='380px' alt="示例1">

<img align="left" src="https://ghproxy.com/https://raw.githubusercontent.com/FrostN0v0/kirami-plugin-qweather/master/example2.jpg" width='380px' alt="示例2">

<img align="left" src="https://ghproxy.com/https://raw.githubusercontent.com/FrostN0v0/kirami-plugin-qweather/master/example3.jpg" width='380px' alt="示例3">