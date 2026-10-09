# 奥德赛实况转绘 (`mario-odyssey-transfer`) v1.0.0

把实拍照片一键转成《超级马力欧：奥德赛》Switch 实机截图风格：玩具般圆润的 3D 渲染、金币/能量月亮计数 HUD、中文游戏 UI，附可复用的转绘提示词模板。

Transform real-world reference photos into Super Mario Odyssey in-game screenshot prompts or generated images with maximum Odyssey rendering fidelity. Use when the user provides landscape, city, street, park, beach, desert, snow, food, selfie, pet, or travel photos and asks for Mario Odyssey screenshot transfer, photo-to-gameplay prompt writing, image-to-image prompts, Link-style HUD with moons and coins, or reusable real-photo-to-Odyssey workflows.

## 文件结构

- `SKILL.md` —— skill 定义（含完整转绘提示词配方 / 工作流）
- `agents/openai.yaml` —— agent 配置
- `icon.png` —— skill 定制图标

## 使用方式

将本仓库作为 skill 包使用：把 `SKILL.md`、`agents/`、`icon.png` 放入你的 skill 目录即可。也已同步上架 [skillhub.cn](https://skillhub.cn) 与 ModelScope（魔搭社区），搜 `mario-odyssey-transfer` 即可找到。

## 声明

粉丝自制、非商业用途的 prompt 工作流，仅用于个人学习与研究，与相关权利方无关。输出内容请勿用于商业售卖、广告或暗示官方授权的场景。

## License

MIT
