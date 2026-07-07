# jimengskill_fast

把抖音/小红书等视频素材快速整理成可复用的即梦 Skill。

这个仓库沉淀了三类内容：

- 本地视频抽帧归档工具
- 视频素材到 Skill 的整理工作流
- 已经整理好的即梦 Skill 示例

## 快速开始

1. 打开 `tools/video-frame-archive.html`
2. 选择录屏或视频文件
3. 填入原链接/来源文案
4. 抽帧后手动排除无效帧
5. 下载 ZIP 归档
6. 把 ZIP 交给 AI 做文案精选和 Skill 生成

工具默认不上传视频，所有抽帧在浏览器本地完成。

## 目录

```text
tools/
  video-frame-archive.html              本地视频抽帧归档工具

skills/
  anthropomorphic-pet-vlog.md           强拟人萌宠旅行 Vlog 快切生成
  healing-original-ip-incubator.md       治愈系原创 IP 孵化助手
  original-ip-healing-food-video.md      原创 IP 治愈生活美食短片生成
  director-asset-prompt-generator.md     导演式人物场景资产提示词生成
  nostalgic-era-video-generator.md       年代感第一人称怀旧短片生成
  contrast-reversal-ad-generator.md      强钩子反转广告叙事生成
  avant-garde-real-human-portrait.md     先锋真实感 AI 人像摄影
  jimeng-face-sculpting.md               人像捏脸提示词生成

examples/
  cat_vlog/                             萌宠拟人 Vlog 案例
  mushroom_life/                        小蘑菇治愈日常案例
  asset_prompt/                         资产提示词拆解案例

docs/
  workflow.md                           完整工作流
  jimeng-skill-generation-rules.md       即梦 Skill 生成规则和 GPT 提示词
  visual-elements-formula.md             画面元素描写公式
  nostalgic-video-formulas.md            年代感视频公式和镜头库
  avant-garde-portrait-realism.md        先锋 AI 人像去塑料感笔记

templates/
  video-to-skill-tracker.xlsx            素材登记表
```

## 当前沉淀的 Skill

- `强拟人萌宠旅行Vlog快切生成`
  - 解决普通“猫出现在地铁/商场/公园”不够拟人的问题。
  - 强制生成 0-2s 时间轴分镜、景别、镜头、动作、道具和负面约束。

- `治愈系原创IP孵化助手`
  - 帮普通创作者从零设计一个有记忆点、可持续拍内容的治愈系原创 IP。

- `原创IP治愈生活美食短片生成`
  - 把原创角色放入微缩生活场景，生成治愈生活/美食短片。

- `导演式人物场景资产提示词生成`
  - 从简单创意拆解人物、场景、道具、色彩和镜头用途，再生成高质量资产 Prompt。

- `年代感第一人称怀旧短片生成`
  - 把童年、亲情、老街、市井、校园等怀旧主题拆成生图资产、人物一致性、时间轴分镜和镜头运动。
  - 强制使用年代物件、第一人称代入、VHS/CRT旧影像质感、环境同期声和连续叙事。

- `强钩子反转广告叙事生成`
  - 根据产品卖点选择“生活误判反差”或“超现实痛点具象化”。
  - 支持紫外线恶魔、防晒护盾、干裂沙漠、牛奶绿洲等痛点可视化，但禁止无关炫技特效。

- `先锋真实感AI人像摄影`
  - 通过皮肤毛孔、五官不对称、不均匀光影、衣物磨损、原生相机瑕疵来去除 AI 人像塑料感。
  - 适合先锋时装摄影、街拍感人像、杂志实验影像和真实感人物资产。

- `人像捏脸提示词生成`
  - 把猫系脸、狐系脸、反派脸、清冷脸、幼态脸等审美标签拆成脸型、三庭五眼、眼型、鼻子、嘴唇、折叠度、气质和妆容。
  - 适合生成即梦 text2image/image2image 的写实人像捏脸 Prompt，避免只写抽象脸谱词。

## 抽帧工具能力

`tools/video-frame-archive.html` 支持：

- 本地选择视频
- 快速跳帧抽样
- seek 失败时切换实时播放抽帧
- 手动排除/恢复不需要的帧
- 生成 contact sheet
- 生成 `manifest.json`
- 可选标记“需要音频转文字”
- 可选粘贴已有转写稿
- 尝试导出 `audio.wav`
- 下载 ZIP 归档

## 推荐素材交接格式

最终给 AI 的 ZIP 应包含：

```text
manifest.json
note.md
contact_sheet.png
frames/
transcript.txt      可选
audio.wav           可选
```

## 注意

- 浏览器本地工具不内置稳定语音识别。
- 若需要转写，可先用剪映、飞书妙记、Whisper 等工具生成文本，再粘贴到工具中归档。
- 公开发布 Skill 时建议保留原视频来源链接，并避免大段照搬创作者原文。
