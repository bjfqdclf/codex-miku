# Codex Miku Pet

一个适用于 Codex 自定义桌面宠物的 Hatsune Miku 风格像素宠物资源包。

仓库地址：`git@github.com:bjfqdclf/codex-miku.git`

<p align="center">
  <img src="assets/miku-pet-cover.png" alt="Codex Miku Pet" width="420">
</p>

## 内容

这个仓库包含可直接安装的宠物包，以及生成过程中的验证和预览产物。

```text
package/
  pet.json
  spritesheet.webp
assets/
  miku-pet-cover.png
run/
  final/
    validation.json
    spritesheet.webp
  qa/
    contact-sheet.png
    videos/
```

- `package/pet.json`：Codex 宠物元信息，包含 `id`、展示名称、描述和精灵图路径。
- `package/spritesheet.webp`：可直接使用的透明背景动画精灵图。
- `assets/miku-pet-cover.png`：GitHub README 头图。
- `run/qa/contact-sheet.png`：所有动作帧的总览图，适合在 GitHub 页面快速预览。
- `run/qa/videos/`：各动作的本地预览视频。
- `run/final/validation.json`：精灵图验证结果。

## 动作状态

| 状态 | 动画介绍 | 首帧 | 预览 |
| --- | --- | --- | --- |
| `idle` | 默认待机状态，轻微呼吸和站立动作，适合日常陪伴。 | <img src="run/frames/idle/00.png" alt="idle" width="72"> | [idle.mp4](run/qa/videos/idle.mp4) |
| `running` | 通用跑步循环，用在移动或过渡时，动作更活泼。 | <img src="run/frames/running/00.png" alt="running" width="72"> | [running.mp4](run/qa/videos/running.mp4) |
| `running-right` | 向右移动时的跑步动画，双马尾随动作摆动。 | <img src="run/frames/running-right/00.png" alt="running-right" width="72"> | [running-right.mp4](run/qa/videos/running-right.mp4) |
| `running-left` | 向左移动时的跑步动画，与右移动方向保持一致的镜像表现。 | <img src="run/frames/running-left/00.png" alt="running-left" width="72"> | [running-left.mp4](run/qa/videos/running-left.mp4) |
| `waving` | 挥手打招呼，适合作为唤醒、互动或欢迎动作。 | <img src="run/frames/waving/00.png" alt="waving" width="72"> | [waving.mp4](run/qa/videos/waving.mp4) |
| `waiting` | 等待状态，动作更克制，适合任务排队或短暂停顿。 | <img src="run/frames/waiting/00.png" alt="waiting" width="72"> | [waiting.mp4](run/qa/videos/waiting.mp4) |
| `jumping` | 跳跃动作，表现开心、确认或轻量反馈。 | <img src="run/frames/jumping/00.png" alt="jumping" width="72"> | [jumping.mp4](run/qa/videos/jumping.mp4) |
| `review` | Review 场景动作，适合 Codex 正在检查、阅读或思考时展示。 | <img src="run/frames/review/00.png" alt="review" width="72"> | [review.mp4](run/qa/videos/review.mp4) |
| `failed` | 失败或出错反馈动作，用于任务失败时的可爱状态提示。 | <img src="run/frames/failed/00.png" alt="failed" width="72"> | [failed.mp4](run/qa/videos/failed.mp4) |

## 安装

克隆仓库：

```bash
git clone git@github.com:bjfqdclf/codex-miku.git
cd codex-miku
```

安装到 Codex pets 目录：

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/pets/hatsune-miku"
cp package/pet.json package/spritesheet.webp "${CODEX_HOME:-$HOME/.codex}/pets/hatsune-miku/"
```

安装完成后的目录应为：

```text
${CODEX_HOME:-$HOME/.codex}/pets/hatsune-miku/
  pet.json
  spritesheet.webp
```

然后在支持自定义宠物的 Codex 环境中选择或加载 `hatsune-miku`。

## 宠物信息

| 字段 | 值 |
| --- | --- |
| Pet ID | `hatsune-miku` |
| Display Name | `Hatsune Miku` |
| Spritesheet | `1536x1872` WEBP RGBA |
| Layout | `8x9` atlas |
| Validation | `run/final/validation.json` 中 `ok` 为 `true` |

## 说明

这是一个非官方的自定义 Codex 宠物资源包。角色造型灵感来自 Hatsune Miku，仅用于个人桌面宠物展示和本地 Codex 自定义体验。
