# 全局配置说明

本工具读取 `config/config.json` 作为全局配置文件。可用字段如下：

- `user`: 当前登录用户标识（内部使用）。
- `pdir_id`: 保存位置的文件夹ID（内部使用）。
- `dir_name`: 保存位置的文件夹名称（内部使用）。
- `share_interval_seconds`: 分享成功后进行限流等待的秒数，默认 `5`。

示例配置：

```json
{
  "user": "Lai",
  "pdir_id": "0",
  "dir_name": "根目录",
  "share_interval_seconds": 5
}
```

说明：

- 限流等待仅在“成功创建分享链接”后触发，失败不会等待，仍按重试节奏执行。
- 修改 `share_interval_seconds` 后，重新运行脚本即可生效。