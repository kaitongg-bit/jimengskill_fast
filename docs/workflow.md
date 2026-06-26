# 视频素材到即梦 Skill 工作流

## 目标

把收藏的视频、录屏、截图和原链接整理成：

1. 视频文案精选
2. 可复用方法论
3. 标准即梦 Skill Markdown

## 输入

最小输入：

- 原视频链接
- 录屏文件
- 抽样截图或 contact sheet

可选输入：

- 人工截图
- 音频转写稿
- 已有提示词
- 博主原始文案

## 推荐流程

### 1. 本地抽帧归档

使用：

```text
tools/video-frame-archive.html
```

操作：

1. 选择录屏
2. 填原链接和来源文案
3. 选择抽帧间隔和最多帧数
4. 抽帧完成后排除无效帧
5. 如需要音频转文字，勾选“需要音频转文字”
6. 下载 ZIP 归档

### 2. AI 读取归档

AI 读取：

- `manifest.json`
- `note.md`
- `contact_sheet.png`
- `frames/`
- `transcript.txt`

### 3. 生成视频文案精选

精选稿应包含：

- 来源链接
- 原始文案
- 素材说明
- 画面观察
- 转写重点
- 核心价值
- 推荐工具链
- 建议表单字段
- 可复用 Prompt 骨架
- 生成 Skill 时的注意事项

### 4. 抽象成 Skill

不要只复刻单条视频，应判断它属于哪类可复用能力：

- 角色孵化
- 强拟人 Vlog
- 治愈生活短片
- 美食流程短片
- 资产提示词生成
- 年代感怀旧短片
- 绿幕素材生成
- 分镜/镜头/构图方法

### 5. 输出即梦 Skill

标准结构：

```markdown
---
name: 技能名称
description: 技能描述
---
# 技能名称

## 角色定位
## 工具使用规范
## 执行流程
## Prompt 设计规范
## 表单设计规范
## 全局约束
```

## 判断原则

### 不要写窄

例如“小蘑菇吃面”不应该只做成吃面 Skill，而应抽象为：

```text
原创 IP 治愈生活美食短片生成
```

### 不要写空

例如“宠物 Vlog”太空，应强化：

```text
强拟人行为 + 快切时间轴 + 景别镜头 + 道具 + 负面约束
```

### 先看真正难点

普通人做不出小蘑菇这样的原创 IP，难点不是“把角色放进场景”，而是先设计出一个讨喜、可记忆、可持续更新的角色。

## 当前案例

### 猫拟人 Vlog

位置：

```text
examples/cat_vlog/
skills/anthropomorphic-pet-vlog.md
```

重点：

- 地点必须映射为人类行为。
- Prompt 必须按 0-2s 时间轴写。
- 公园不能写猫躺着打滚，要写野餐、看地图、自拍。

### 小蘑菇治愈日常

位置：

```text
examples/mushroom_life/
skills/original-ip-healing-food-video.md
```

重点：

- 原创 IP 角色
- 微缩童话世界
- 生活流程
- 美食收尾

### 资产提示词

位置：

```text
examples/asset_prompt/
skills/director-asset-prompt-generator.md
```

重点：

- 先拆资产，不是直接堆长 Prompt。
- 画面元素要包含全景定位、主体结构、功能设施、地标视觉锚点、生活痕迹。

### 年代感视频

位置：

```text
docs/nostalgic-video-formulas.md
skills/nostalgic-era-video-generator.md
```

重点：

- 年代感不是只加滤镜，要写具体时代物件、生活动作和环境音。
- 先做生图资产和人物一致性，再进入图生视频。
- 视频 Prompt 必须按时间戳写主体、动作、场景、镜头、台词或环境音。
- 第一人称 POV 要有镜头高度、手部/随身物件等身体代入。
