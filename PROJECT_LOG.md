# 超模项目 (Supermodel Project) - 档案

## 项目概述
- **目标**：建立标准化的高端服装模特图生成工作流 (SOP)。
- **核心资产**：
  - **路径**：`D:\Supermodel_Project`
  - **展示页**：`D:\Supermodel_Project\index.html` (深色模式/全屏预览/参数溯源)
  - **图片库**：`D:\Supermodel_Project\images` (仅保留最终成品)

## 核心资产库 (Assets)

### 1. 模特库 (Face Library - 1:1 Square)
*全部锁定为 22-26 岁，冷峻(Stoic)表情，纯色背景*
- **Model 5 (French)**: 法式优雅，棕色波浪发，经典脸。
- **Model 6 (Blonde)**: 金发蓝眼，柔美清纯，适合浅色系。
- **Model 7 (Redhead)**: 斯堪的纳维亚风，红发雀斑，自然感。
- **Model 8 (Eastern European)**: 东欧骨相，黑发深棕眼，高级感强。
- **Model 9 (British)**: 英伦风，深色卷发，沉稳大气。

### 2. 场景库 (High-end Scenes - 9:16 Vertical)
*全部为纯净无道具(Empty)、无缝循环墙(Cyc Wall)、顶级光影*
- **Luxury Beige**: 暖米色石膏质感，带建筑阴影。
- **Sage Green**: 高级鼠尾草绿，柔和漫射光。
- **Muted Clay**: 莫兰迪粘土色，大地质感。
- **Cool Gray**: 冷灰色质感，带百叶窗光影。

---

## 标准操作流程 (SOP) - V4 级标准

### 1. 素材准备
- **服装图**：必须包含 **全貌图 (Full View)** 和 **细节图 (Detail View)**。
- **核对**：生成前必须**肉眼核对**服装的真实颜色和纹理（切勿凭印象瞎编颜色，如将条纹误判为纯色）。

### 2. 合成参数规范
- **模型**：`nano-banana-pro` (Gemini 3 Pro Image)
- **分辨率**：2K (Upscaled)
- **比例**：9:16 (Vertical)
- **输入源 (Input Images)**：必须同时包含以下 **4 张**：
  1. `Face Reference` (模特脸)
  2. `Clothing Full` (服装全貌)
  3. `Clothing Detail` (关键细节，如Logo/刺绣)
  4. `Scene Background` (纯净场景)

### 3. 提示词 (Prompt) 黄金公式
```text
High-end fashion editorial, [Model Name/Type] in [Scene Name].
EXTREME DETAIL: [Specific clothing details, e.g., crisp embroidery, texture].
EXTREME REALISM: 
- Shadows MUST wrap naturally around body curves (Light Wrap).
- Soft shadow edges (Penumbra).
- Subsurface scattering on skin.
- Realistic ground contact shadows (Ambient Occlusion).
9:16 vertical, 8k.
```

### 4. 质量自检标准 (QC Checklist)
- [ ] **融合度**：光影方向是否与背景一致？是否有“贴图感”？
- [ ] **物理逻辑**：脚部是否有接触阴影？阴影是否随身体起伏变形？
- [ ] **细节还原**：Logo/刺绣是否清晰？文字是否可读？
- [ ] **人脸一致**：是否保持了原模特的特征（不被过度美颜）？

## 历史里程碑
- **2026-02-09**：项目启动。
- **V2 阶段**：解决了场景穿帮问题，确立了纯净影棚标准。
- **V3 阶段**：攻克了“光影融合”难题，引入 Light Wrap 和 Penumbra 概念。
- **V4 阶段**：(当前标准) 引入 Detail Reference，解决了微小图案（如猫咪刺绣）模糊的问题。
