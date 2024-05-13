# NoneBot-Tsugu

## 介绍
基于 tsugu-bangdream-bot 的 NoneBot2 插件, 用于查询 BanGDream 手游的相关信息

## 功能
请参考 [关于 Tsugu V3.0](https://www.bilibili.com/read/cv18082802)

## 安装方法
<details open>
<summary>使用 nb-cli 安装</summary>
在 nonebot2 项目的根目录下打开命令行, 输入以下指令即可安装

    nb plugin install nonebot-tsugu
</details>

<details>

<summary>使用包管理器安装</summary>
在 nonebot2 项目的插件目录下, 打开命令行, 根据你使用的包管理器, 输入相应的安装命令
<details>
<summary>pip</summary>

    pip install nonebot-tsugu
</details>
打开 nonebot2 项目根目录下的 `pyproject.toml` 文件, 在 `[tool.nonebot]` 部分追加写入

    plugins = ["nonebot_plugin_tsugu"]
</details>
</details>

## 配置
| 配置项 | 值 | 说明 |
| --- | --- | --- |
| api_base | "http://tsugubot.com:8080" | Tsugu 后端地址 |
| use_easy_bg | "True" | 是否使用简易背景 |
| compress | "True" | 是否压缩图片 |
| bot_name | "Tsugu" | Bot名称 |
| bandori_station_token | "ZtV4EX2K9Onb" | 车站 Token |
| token_name | "token" | Token 名称 |
| api_use_proxy | "False" | 是否使用代理访问 Tsugu 后端 |
| proxy_url | "http://127.0.0.1:7890" | 代理地址 |
| server_list | 格式见下文 | 服务器列表 |
| ban_gacha_simulate_group_data | [] | 禁止模拟抽卡的群 |
| enable_carNum_prompt_groups | [] | 启用车牌上传提示的群 |
| cmd_list | 格式见下文 | Tsugu命令列表 |

### 服务器列表格式 (修改只需修改别名)
```json
{
    "0": ["日服","jp",其他别名......],
    "1": ["国际服","en",其他别名......],
    "2": ["台服","tw",其他别名......],
    "3": ["国服","cn",其他别名......],
    "4": ["韩服","kr",其他别名......]
}
```

### 命令列表格式 (修改只需修改触发指令与是否启用)
```json
{
    [
        { 
            "command_name": ["触发指令1","触发指令2".....],
            "ifEnable":"是否启用(True/False)",
            "name":"指令功能"
        },
        ......
    ]
}
```

## 鸣谢
- [tsugu-bangdream-bot](https://github.com/Yamamoto-2/tsugu-bangdream-bot) Tsugu 本体
