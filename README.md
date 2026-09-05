# dannywsh/skills

用户装的是这些仓库本身。不要装上游 fork 源。更新用 `npx skills update`。

```bash
npx skills add dannywsh/video-use-ad -g -y
npx skills add dannywsh/biliup -g -y
npx skills update -g -y
```

| 安装源 | skill 名 | 做什么 |
|--------|----------|--------|
| `dannywsh/video-use-ad` | `video-use` | 对话剪辑视频、B 站商品宣传片；嵌套 `skills/bili-cover/`（自带生图 → gcp-gemini → ark-seedream） |
| `dannywsh/biliup` | `biliup` | B 站登录、投稿、下载、评论、会员购/票务挂载 |

独立 `byted-ark-seedream-skill` 已停用：封面和 Seedream 调用都在 `video-use` 的 `bili-cover` 里，不要再 `npx skills add` 那个 skill。

`video-use` 装好后自带 `bili-cover`。密钥写在该 skill 根目录 `.env`（全局安装一般是 `~/.agents/skills/video-use/.env`），不要提交。封面相关键：`GCP_GEMINI_IMAGE_API_KEY`、`ARK_SEEDREAM_API_KEY`。`npx skills update` 可能整目录替换已安装文件，更新后检查 `.env` 是否还在。
