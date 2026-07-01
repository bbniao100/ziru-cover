# ziru-cover

子儒封面是一个 Codex skill，用于把视频脚本、选题和主图转化成高点击、高转化的中文社交媒体封面方案。

它适合小红书封面、抖音/视频号封面、公众号主图、课程/训练营推广封面，以及任何需要从“脚本 + 主图”快速产出封面策略、设计提示词或成图的场景。

## 能做什么

- 从视频脚本里提炼点击理由
- 生成主标题、副标题、标签和氛围小字
- 选择适合的版式模型
- 输出点击优先、专业优先、转化优先 3 个方向
- 如果当前智能体能调用图像模型，直接生成或编辑封面
- 如果当前智能体不能调用图像模型，输出完整提示词，方便复制到 ChatGPT Image / image2 / 其他官方生图工具

## 安装

### 方式一：普通安装

在 Codex 或终端中运行：

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo bbniao100/ziru-cover \
  --path . \
  --name ziru-cover
```

安装后重启 Codex。

### 方式二：方便未来同步更新

如果你希望以后通过 `git pull` 同步更新，可以直接克隆到本地 skills 目录：

```bash
cd ~/.codex/skills
git clone https://github.com/bbniao100/ziru-cover.git ziru-cover
```

更新时运行：

```bash
cd ~/.codex/skills/ziru-cover
git pull
```

如果你本地已经存在同名 `ziru-cover` skill，请先备份或替换旧目录。

## 调用方式

安装并重启 Codex 后，可以这样使用：

```text
用 $ziru-cover，把这个视频脚本和主图做成 3 个高点击封面方向。
```

也可以自然语言调用：

```text
用子儒封面，根据这个脚本和主图生成小红书封面。
```

```text
用子儒主图，给我一个能复制到 ChatGPT Image 的完整生图提示词。
```

## 推荐输入

```text
平台：小红书
目标：提高点击和私信咨询
视频脚本：……
主图：……
风格偏好：干净、有设计感、标题要强
```

只提供脚本和主图也可以，skill 会默认按移动端中文信息流封面处理。

## 搜索关键词

在 GitHub 可以搜索：

- ziru-cover
- 子儒封面
- 子儒主图
- Codex skill 高点击封面
- Xiaohongshu cover Codex skill
- Chinese social media cover skill

## 更新机制

这个仓库是 skill 的源头版本。

- 新用户安装时会获得 GitHub 上的最新版本。
- 已经普通安装过的用户，本地不会自动更新，需要重新安装或替换本地目录。
- 使用 `git clone` 安装的用户，可以通过 `git pull` 同步更新。

## Skill 名称

安装后 skill 名称是：

```text
$ziru-cover
```

展示名是：

```text
子儒封面
```
