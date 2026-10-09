---
name: mario-odyssey-transfer
slug: mario-odyssey-transfer
displayName: 奥德赛实况转绘
version: 1.0.0
summary: "把实拍照片一键转成《超级马力欧：奥德赛》Switch 实机截图风格：玩具般圆润的 3D 渲染、金币/能量月亮计数 HUD、中文游戏 UI，附可复用的转绘提示词模板。"
license: MIT
icon: icon.png
description: "Transform real-world reference photos into Super Mario Odyssey in-game screenshot prompts or generated images with maximum Odyssey rendering fidelity. Use when the user provides landscape, city, street, park, beach, desert, snow, food, selfie, pet, or travel photos and asks for Mario Odyssey screenshot transfer, photo-to-gameplay prompt writing, image-to-image prompts, Link-style HUD with moons and coins, or reusable real-photo-to-Odyssey workflows."
---

# 马里奥奥德赛实况转绘

Convert real-world reference photos into **Nintendo Switch Super Mario Odyssey gameplay screenshots**. The priority is **MAXIMUM ODYSSEY IN-GAME RENDERING FIDELITY**: bright, chunky, toy-like 3D game-engine output, not illustration, anime art, painting, poster art, cinematic CG, or photorealism.

This is a fan-made, non-commercial workflow for personal learning, research, and prompt testing only. It is not affiliated with, endorsed by, sponsored by, or approved by Nintendo, Super Mario, Super Mario Odyssey, or any related rights holders. Do not use outputs for commercial sale, advertising, merchandising, paid services, or uses that imply official authorization.

## Output Mode

- If the user asks for prompts, return the final prompt in one code block unless they ask for explanation.
- If the user asks to generate images, use the available image generation workflow.
- If generating from a reference photo, generate first, then provide the final prompt unless the user asks for image only.
- If both prompt and image are requested, generate first, then provide the prompt.
- Use Chinese for user-facing final prompts, but keep the English rendering-control blocks exactly because they strongly steer image models.

## Reference Analysis

Before writing the prompt, identify only what affects transfer:

- Core subject: city street, park, beach, desert, snowfield, forest, lake, plaza, restaurant interior, market, landmark, etc.
- Recognizable features to preserve: skyline, building silhouette, terrain shape, water path, road, bridge, stair, tree line, horizon.
- Kingdom mapping: map the real scene to the closest Odyssey kingdom theme — city → 都市之国 (New Donk City), desert → 沙之国, forest → 森林之国, snow → 雪之国, beach → 海之国, ruins → 失落之国, plaza/park → 蘑菇王国.
- Scene type: exploration, rest, interaction, meal, travel, celebration, photo moment.
- Environment: time, weather, season, visibility.
- UI needs: light HUD (coins/moons), snapshot-mode frame, or no UI.
- Modern people, vehicles, signs, roads, barriers, and facilities that must be removed or converted into kingdom props.

Preserve the reference photo's identity. Improve it into a playable Odyssey moment, not a poster.

## Planning Workflow

Before filling the final prompt, decide:

1. 场景类型与王国映射：探索 / 休息 / 互动 / 聚餐 / 旅行 / 庆祝，对应哪个王国主题
2. 环境设定：时间 / 天气 / 季节
3. 角色模式：默认将照片人物转译为奥德赛风格原创王国冒险者（圆润体型、表情生动、鲜艳服装）；或马里奥式红帽蓝背带装；或无角色纯风景
4. UI 需求：轻量 HUD（金币/月亮计数）/ 快照模式相框 / 无 UI
5. 构图和视角：远景 / 高机位 / 低机位 / 第三人称跟随 / 近景互动

Do not output this planning checklist unless the user asks. Reflect the decisions in the final prompt.

## Prompt Template

When a reference image is provided, always derive concrete content from the image. Never output placeholders.

Use this order for prompt-only output and image-generation prompts:

```text
Super Mario Odyssey gameplay screenshot - MAXIMUM ODYSSEY IN-GAME RENDERING FIDELITY.
This must look EXACTLY like actual Odyssey Switch gameplay footage, NOT illustration, NOT anime art, NOT painting.

RENDERING STYLE - ODYSSEY SWITCH IN-GAME (CRITICAL):
VIBRANT SATURATED CHEERFUL colors dominate every surface; CHUNKY ROUNDED toy-like geometry, diorama/playset miniature feel; CLEAN 3D game-engine rendering; soft ambient occlusion ONLY, gentle and even; GLOSSY specular highlights on smooth surfaces; bold readable silhouettes; smooth rounded edges everywhere; NO photorealistic texture, NO gritty detail, NO painting texture.

SCENE：保留<参考图核心构图、主体、地形、道路/水面/建筑/天空等识别特征>，映射为<王国主题>；现代设施和游客做王国化转译或移除；画面尺寸比例：9:16，1440x2560
CHARACTER AND GAMEPLAY：<默认：照片人物转译为奥德赛风格原创王国冒险者，圆润体型、表情生动、鲜艳服装，对标奥德赛角色的比例、材质简洁度和动作可信度；或：马里奥式红帽蓝背带装>；<一句话写清动作>
MARIO ELEMENTS：<3-7 个场景适配元素，只列名称，如：能量月亮、金币、问号砖块、绿色水管、检查点旗帜、帽子附身目标>
UI：<按需加入轻量 HUD / 快照模式相框>；所有可读 UI 使用中文，按键动词只用中文；场景内真实招牌和广告转为不可读王国纹样或 1-3 字中文

LIGHTING - ODYSSEY GAME ENGINE STYLE:
Bright CHEERFUL daylight, vivid and high-clarity; soft even shadows, NOT dramatic, NOT cinematic; gentle warm sunlight with glossy highlights; simple flat illumination with subtle directional hints; Overall BRIGHT and clearly visible; NO HDR, NO photorealistic lighting, NO complex light rays.

COLOR PALETTE - ODYSSEY <王国主题>:
<元素1>: Bold saturated <base color>, clean and vivid
<元素2>: Chunky <color> masses with glossy highlights
Sky: bright cyan-blue, 2-3 tones maximum; all colors CLEAN, BRIGHT, highly saturated; cheerful and inviting.

MATERIALS - CHUNKY TOY-LIKE SURFACES:
<材质1>: smooth rounded surfaces with glossy highlights, NO texture complexity, NO fine surface detail
<材质2>: chunky <color> volumes, clean edges, toy-like finish
<材质3>: simple <color> base with soft shading, smooth and polished

PARTICLE EFFECTS - ODYSSEY STYLE:
<仅在有花瓣/纸屑/水花/烟火/月亮光效时填写；simple geometric sparkles and soft round particles, clean digital game style, NOT realistic>

STRICT SELF-CHECK TARGET:
The final image must pass: every surface uses chunky rounded toy-like forms; colors are vibrant, saturated, and cheerful; lighting is bright, even, and clearly readable; silhouettes are bold game-engine shapes; materials are smooth and glossy without photoreal texture, gritty noise, or microdetail; scene-specific microdetail is suppressed; UI is subtle Chinese gameplay UI only and never reads as a poster title; reference composition, landmark scale, camera angle, terrain/water/building relations, environmental density, and gameplay action are preserved; if original characters are used, they must read as Odyssey in-game kingdom adventurers, not modern photo people or fashion illustrations.

FINAL EMPHASIS - MUST LOOK LIKE ACTUAL ODYSSEY SWITCH GAMEPLAY:
Chunky rounded toy-like forms. Vibrant saturated cheerful colors. Bright even lighting. NO fine detail, NO texture complexity. CLEAN 3D GAME RENDERING. Diorama/playset miniature feel. Odyssey Switch in-game screenshot aesthetic. NOT illustration, NOT anime, NOT painting style.
```

Delete the `PARTICLE EFFECTS` block when no particles or special effects apply.

## Required Prompt Fields

Every final prompt must include:

- Scene description: concrete character, action, environment, composition, preserved reference features, and kingdom mapping.
- Character mode: default original kingdom adventurer, Mario-style outfit option, or no character. Original characters must read as Odyssey in-game adventurers benchmarked against Odyssey's chunky proportions and material simplicity.
- `COLOR PALETTE`: main elements, bold and saturated.
- `MATERIALS`: main materials rendered as chunky toy-like surfaces.
- `STRICT SELF-CHECK TARGET`: a compact pass/fail target that names chunky forms, saturated colors, bright lighting, glossy materials, subtle Chinese UI, microdetail suppression, and reference preservation.
- Opening and final emphasis blocks, unchanged in meaning.

Optional:

- `PARTICLE EFFECTS`: include only for petals, confetti, splashes, fireworks, moon glow, or similar effects.

## Style Anchor Rules

Start every image prompt with these two lines:

```text
Super Mario Odyssey gameplay screenshot - MAXIMUM ODYSSEY IN-GAME RENDERING FIDELITY.
This must look EXACTLY like actual Odyssey Switch gameplay footage, NOT illustration, NOT anime art, NOT painting.
```

Then include `RENDERING STYLE - ODYSSEY SWITCH IN-GAME (CRITICAL)` before scene content. Include `STRICT SELF-CHECK TARGET` after particles/materials and before final emphasis. End every prompt with `FINAL EMPHASIS - MUST LOOK LIKE ACTUAL ODYSSEY SWITCH GAMEPLAY`.

Do not scatter extra style essays across the prompt. Rendering control lives in the opening, lighting, color, materials, particles, and final emphasis blocks.

## Odyssey Rendering Calibration

Default to Odyssey Switch gameplay:

- Bright, saturated, cheerful, clearly playable, and game-rendered.
- Clean daylight: vivid cyan-blue sky, lush chunky green grass masses, bold reds and yellows, glossy highlights.
- Chunky rounded toy-like geometry on every surface; diorama/playset miniature feel.
- Clean 3D rendering with soft ambient occlusion only; no photorealistic texture.
- Grass appears as bright chunky color masses, not individual photographic blades.
- Trees appear as clustered rounded volumes, not individually detailed leaves.
- Rocks, buildings, roads, and water use smooth low-frequency surfaces, not cracks, pores, or grain.
- Distant elements are lighter, softer, and lower contrast with cheerful atmospheric perspective.
- Characters have bold readable silhouettes, expressive faces, and smooth shaded color planes.
- Signature props: golden Power Moons (crescent), spinning gold coins, ? Blocks, green warp pipes, Checkpoint flags.

UI guidance:

- Use subtle Odyssey-style HUD as a realism anchor: coin counter and Power Moon counter top-right, health indicator top-left, Chinese action prompts where relevant.
- Snapshot-mode frame is allowed for photo-moment scenes: rounded corners, filter name in Chinese.
- UI must look like game state, not graphic design decoration, and never read as a poster title.
