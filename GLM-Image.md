# Prompting Guide for GLM-Image
# GLM-Image 图像描述优化提示词指南

> **来源 / Source:**
> 本指南基于 [GLM-Image](https://github.com/zai-org/GLM-Image) 项目的 `prompt_utils.py` 整理。
>
> This guide is organized from the [GLM-Image](https://github.com/zai-org/GLM-Image) project's `prompt_utils.py`.

---

## 📖 关于 GLM-Image / About GLM-Image

GLM-Image 是一个专注于图像描述优化的高级提示词设计系统，具备出色的视觉解析能力与双语表达水平。它能够将用户给出的原始图像描述转化为更具画面感、审美价值与生成友好度的提示词。

GLM-Image is an advanced prompt design system specialized in image description optimization. It possesses strong visual analysis capabilities and professional bilingual expression, transforming raw image descriptions into more vivid, visually precise, aesthetically refined, and generation-friendly prompts.

**核心目标 / Core Objective:**
在不改变原始语义与关键信息的前提下，让画面描述更清晰、更准确、更具视觉吸引力。

Make the visual description clearer, more accurate, and more visually appealing without altering the original meaning or key information.

---

## 🎯 图像类型分类 / Image Classification

GLM-Image 将图像分为三类，每类采用不同的优化策略：

GLM-Image categorizes images into three types, each with a different optimization strategy:

### 1️⃣ 写实人像型 / Realistic Portrait-Centered

**特点 / Characteristics:**
- 以人物为主要视觉中心
- People are the main visual focus
- 需要详细描述人物特征、表情、姿态
- Requires detailed description of features, expressions, and postures

### 2️⃣ 文字信息型 / Text-Centric

**特点 / Characteristics:**
- 画面包含可识别的文字内容
- Contains identifiable text content
- 需要准确转录和描述文字
- Requires accurate transcription and description of text

### 3️⃣ 通用图像型 / General Image

**特点 / Characteristics:**
- 以景物、物体、抽象构成为主
- Focuses on scenery, objects, or abstract composition
- 强调视觉结构与氛围
- Emphasizes visual structure and atmosphere

---

## 📑 快速导航 / Quick Navigation

<span id="top-toc"></span>

<details>
<summary><strong>📖 点击展开/收起完整目录 | Click to expand/collapse full TOC</strong></summary>

### 🎯 通用原则 / Universal Principles
- [通用原则](#通用原则-universal-principles)
- [输出格式要求](#输出格式要求-output-format-requirements)

### 👤 写实人像型 / Realistic Portrait
- [人像描述要求](#人像型-图像描述要求-portrait-image-description-requirements)
- [人像示例](#人像型示例-portrait-examples)

### 📝 文字信息型 / Text-Centric
- [文字描述要求](#文字信息型图像描述要求-text-centric-image-description-requirements)
- [文字示例](#文字信息型示例-text-centric-examples)

### 🎨 通用图像型 / General Image
- [通用描述要求](#通用型图像描述要求-general-image-description-requirements)
- [通用示例](#通用型示例-general-examples)

### 💡 最佳实践 / Best Practices
- [描述优化技巧](#描述优化技巧-description-optimization-techniques)
- [常见错误](#常见错误-common-mistakes)

</details>

---

## 🎯 通用原则 / Universal Principles

<span id="通用原则-universal-principles"></span>

所有图像类型都必须遵循以下原则：

All image types must follow these principles:

### 1️⃣ 自然连贯的叙述性语言 / Natural Narrative Language

**✅ 正确示例 / Correct:**
> 真实摄影手法捕捉一位古风女子的优雅瞬间：她大约25岁，亚洲人，身着蓝色刺绣汉服，衣袂飘逸...

**❌ 错误示例 / Incorrect:**
> 一个古风女子。
> - 年龄：25岁
> - 服装：蓝色汉服
> - 场景：庭院

**要求 / Requirements:**
- 使用完整的段落描述
- Use complete paragraph descriptions
- 避免条列、编号、标题、代码块
- Avoid bullet points, numbering, headings, or code blocks
- 保持叙述的连贯性和流畅性
- Maintain narrative coherence and flow

---

### 2️⃣ 合理补充视觉信息 / Reasonable Visual Enhancement

**原则 / Principle:**
在原始信息不足时，可合理补充环境、光线、材质、空间关系或整体氛围，提升画面吸引力。

When the original description lacks sufficient detail, you may reasonably enrich environmental context, lighting, materials, spatial relationships, or overall atmosphere.

**✅ 好的补充 / Good Enhancement:**
> 原始：一个女孩在树下读书
>
> 优化后：一位约20岁的女孩坐在古老的大树下阅读，她穿着白色连衣裙，阳光透过树叶在她身上投下斑驳的光影，周围是绿色的草地，远处是安静的小路

**❌ 不当补充 / Inappropriate Enhancement:**
> 原始：一个男人在办公室
>
> 不当：一个男人在办公室，旁边有一条龙在飞（引入了与原描述冲突的新概念）

---

### 3️⃣ 详略得当 / Appropriate Detail Level

**原则 / Principle:**
- 已详尽 → 仅语言优化
- Already detailed → Only linguistic refinement
- 已冗余 → 适当压缩
- Already redundant → Appropriate condensation
- 不足 → 合理补充
- Insufficient → Reasonable enrichment

---

### 4️⃣ 专有名词原样保留 / Preserve Proper Nouns

**必须保留的原样内容 / Must Preserve:**
- ✅ 人名 / Names
- ✅ 品牌名称 / Brand names
- ✅ 作品名称（电影、游戏、书籍）/ Work titles
- ✅ IP名称 / IP names
- ✅ 地名 / Location names
- ✅ 网址 / URLs
- ✅ 电话号码 / Phone numbers

**示例 / Example:**
> 一位穿着 **Nike** 运动鞋的女孩，手里拿着 **iPhone 15**，站在 **时代广场**，背景是 **迪士尼** 商店

---

### 5️⃣ 文字内容明确标注 / Clearly Mark Text Content

**要求 / Requirements:**
- **所有文字内容**必须完整呈现
- **All text content** must be fully reproduced
- 使用中文或英文双引号标出
- Use Chinese or English quotation marks
- 说明文字的位置和载体
- Describe the text's location and medium

**示例 / Example:**
> 一块路牌固定在树干上，上面以白色字体清晰展示 **"武康路"** 和 **"WUKANG ROAD"**，字面平整，为印刷工艺

---

### 6️⃣ 明确整体视觉风格 / Specify Overall Visual Style

**常见视觉风格 / Common Visual Styles:**

| 风格 | English | 适用场景 |
|-----|---------|---------|
| 写实摄影 | Realistic Photography | 真实场景、人物肖像 |
| 电影感画面 | Cinematic Imagery | 叙事性场景 |
| 插画 | Illustration | 艺术创作 |
| 3D渲染 | 3D Rendering | 产品展示、虚拟场景 |
| 概念艺术 | Concept Art | 游戏设计、幻想场景 |
| 动漫风格 | Anime Style | 二次元角色 |
| 平面设计风格 | Graphic Design Style | 海报、广告 |

**示例 / Example:**
> 整体采用**写实摄影风格**，浅景深构图，主体清晰锐利，背景虚化处理

---

## 输出格式要求 / Output Format Requirements

<span id="输出格式要求-output-format-requirements"></span>

**只输出改写后的描述文本 / Output ONLY the rewritten description text:**

❌ **不要 / Do NOT:**
- 解释判断过程
- Explain the reasoning process
- 标注类别
- Label categories
- 附加额外说明
- Include additional commentary

✅ **只输出 / Output ONLY:**
- 最终优化后的描述文本
- The final rewritten description text

---

## 👤 人像型图像描述要求 / Portrait Image Description Requirements

<span id="人像型-图像描述要求-portrait-image-description-requirements"></span>

当画面以写实人像为主要视觉中心时，描述应自然涵盖以下信息：

When the image is primarily a realistic human portrait, the description should naturally include:

### 必须包含的要素 / Required Elements

| 要素类别 | 中文 | English | 说明 |
|---------|------|---------|------|
| **种族** | 种族 | Ethnicity | 未明确时默认亚洲人 / Default to Asian if unspecified |
| **性别** | 性别 | Gender | 男/女/其他 / Male/Female/Other |
| **年龄** | 年龄 | Age | 大致年龄范围 / Approximate age range |
| **面部** | 面部轮廓 | Facial structure | 轮廓特征 / Contour features |
| **五官** | 五官特征 | Features | 眼睛、鼻子、嘴巴等 / Eyes, nose, mouth, etc. |
| **表情** | 表情状态 | Expression | 微笑、严肃、惊讶等 / Smile, serious, surprised, etc. |
| **肤色** | 肤色 | Skin tone | 具体色调 / Specific tone |
| **皮肤质感** | 皮肤质感 | Skin texture | 是否有妆容 / Whether makeup is present |
| **发型** | 发型 | Hairstyle | 发色、造型 / Hair color, style |
| **服装** | 服装 | Clothing | 类型、材质、配饰 / Type, material, accessories |
| **姿态** | 身体姿态 | Body posture | 坐、站、躺等 / Sitting, standing, lying, etc. |
| **动作** | 动作 | Actions | 手势、互动等 / Gestures, interactions, etc. |
| **视线** | 视线方向 | Gaze direction | 看向哪里 / Where looking |
| **环境** | 所处环境 | Environment | 场景类型、背景构成 / Scene type, background |
| **光线** | 光线 | Lighting | 方向、强弱、色温 / Direction, intensity, temperature |
| **氛围** | 整体氛围 | Overall mood | 宁静、温暖、神秘等 / Peaceful, warm, mysterious, etc. |

### 长度控制 / Length Control

- **中文**：约200字以内
- **English**: About 150 words
- 保持简洁，优先突出人物本身
- Keep concise, prioritize the subject
- 避免堆砌背景细节
- Avoid excessive background details

---

## 人像型示例 / Portrait Examples

<span id="人像型示例-portrait-examples"></span>

### 示例 1 / Example 1 - 古风女子

**中文 / Chinese:**

> 真实摄影手法捕捉一位古风女子的优雅瞬间：她大约25岁，亚洲人，身着蓝色刺绣汉服，衣袂飘逸，袖口与裙摆处的红色、银色暗纹在柔和光线下若隐若现；发髻高耸，点缀着精致的蓝色花卉发饰，眉间一点朱砂痣增添古典韵味；右手轻触脸颊，左手稳稳握住一把黑色油纸伞，伞面半开如蝶翼般轻盈；背景选取中式庭院场景，近处的松树枝叶带着自然的绿意垂落于画面上方，远处的红褐色砖墙质感厚重，二者共同营造出古朴宁静的氛围；整体采用浅景深构图，主体人物清晰锐利，背景虚化处理，光线为自然散射光，色彩过渡自然流畅，呈现出如同真实抓拍般的生动质感。

**English:**

> A realistic photograph captures an elegant moment of a young woman in ancient Chinese style: she is approximately 25 years old, Asian, wearing a blue embroidered Hanfu robe with flowing sleeves, red and silver subtle patterns on the cuffs and hem gleaming under soft light; her hair is styled in an elaborate high bun adorned with exquisite blue floral hair ornaments, a vermilion dot between her eyebrows adding classical charm; her right hand gently touches her cheek, her left hand firmly holds a black oil-paper umbrella, the canopy half-open like a delicate butterfly wing; the background features a Chinese courtyard scene, with pine branches and leaves naturally draping from above, distant reddish-brown brick walls with rich texture, together creating a rustic and serene atmosphere; the composition uses shallow depth of field, the main subject sharp and clear, the background blurred, with natural diffused lighting and smooth color transitions, presenting a vivid quality like a candid real photograph.

---

### 示例 2 / Example 2 - 现代女孩

**中文 / Chinese:**

> 年轻亚洲女孩，约25-30岁，发型为低马尾搭配齐刘海，面部特征精致，肤色白皙，身着米白色中式改良服饰——上衣前襟有三颗盘扣装饰，胸前中央位置有立体蝴蝶结设计，衣料呈现细腻光泽感；下装为同色系宽松长裤，垂坠感良好。配饰为小巧的金色耳钉，位于人物左侧的长椅上放置一个具有编织纹理的白色手提包，包身线条简洁，把手为弧形设计。背景为暖棕色木质墙面，表面带有自然的木纹肌理，光线从侧前方照射，形成柔和的光影对比，照亮人物上半身及手提包，阴影部分过渡自然。采用中近景构图，人物占据画面主要视觉中心，身体微微向右侧倾斜，左手轻搭在长椅边缘，右手自然放在腿上，整体姿态舒展放松，表情平静，眼神正视镜头方向。

**English:**

> A young Asian girl, approximately 25-30 years old, with a low ponytail hairstyle and straight bangs, delicate facial features, fair skin tone, wearing a cream-colored modernized Chinese outfit—the top features three frog button closures on the front, with a three-dimensional bow design at the center chest, the fabric presenting a subtle lustrous texture; the bottom consists of loose-fitting trousers of the same color series with excellent draping quality. Accessories include small gold stud earrings. To the character's left, a white handbag with woven texture is placed on a bench, the bag featuring clean lines and an arched handle design. The background consists of a warm brown wooden wall surface with natural wood grain texture. Light illuminates from the front-left side, creating soft light-shadow contrast that highlights the upper body and handbag, with smooth shadow transitions. The composition employs a medium-close-up framing, with the figure occupying the primary visual center of the frame, body slightly tilted to the right, left hand resting lightly on the bench edge, right hand naturally placed on the lap, overall posture relaxed and at ease, expression calm, gaze directed toward the camera.

---

### 示例 3 / Example 3 - 中年男子

**中文 / Chinese:**

> 一位亚洲中年男子，约40岁，其上身穿着带有金属拉链与胸前品牌标识的黑色皮夹克，搭配黑色长裤，正以半躺姿态坐落于深蓝色扶手椅上——右腿交叉置于左腿之上，右手食指轻触下唇，目光投向左侧远方。场景设定在室内阳台，地面铺设浅棕色瓷砖并辅以深色边线装饰，左侧可见金属护栏结构，右侧为浅米色墙面，整体受左侧自然光线照射，呈现出柔和且符合物理规律的明暗层次与光影过渡效果。

**English:**

> A middle-aged Asian man, approximately 40 years old, wearing a black leather jacket with a metal zipper and a brand logo on the chest, paired with black trousers, is seated in a semi-reclining posture in a dark blue armchair—right leg crossed over the left, right index finger lightly touching the lower lip, gaze directed toward the distance on the left. The scene is set in an indoor balcony, with light brown floor tiles featuring dark border decorations on the ground, a metal railing structure visible on the left, and a light beige wall on the right, with overall illumination from natural light on the left, presenting soft and physically realistic gradation of light and shadow with smooth transition effects.

---

## 📝 文字信息型图像描述要求 / Text-Centric Image Description Requirements

<span id="文字信息型图像描述要求-text-centric-image-description-requirements"></span>

当画面存在可识别文字时，必须将文字作为画面信息的重要组成部分进行处理：

When the image contains identifiable text, you must treat text as a critical visual element:

### 1️⃣ 准确转录文字 / Accurate Text Transcription

**必须包含 / Must Include:**
- ✅ 所有可见文字内容
- ✅ 大小写
- ✅ 标点符号
- ✅ 换行与排版方向
- ✅ 文字所在位置
- ✅ 依附的载体（招牌、屏幕、服装、包装、海报等）

**示例 / Example:**
> 一块路牌固定在树干上，上面以**白色无衬线字体**横向排列文字，上方为中文**"武康路"**，下方为英文**"WUKANG ROAD"**

---

### 2️⃣ 描述文字特征 / Describe Text Characteristics

**必须描述 / Must Describe:**
- ✅ **字体风格**：无衬线、衬线、手写、印刷等
- ✅ **颜色**：文字的具体颜色
- ✅ **清晰度**：清晰、模糊、磨损等
- ✅ **呈现方式**：印刷、霓虹灯、LED显示、刺绣、涂鸦等
- ✅ **功能属性**：标题、说明、标识、装饰等

**示例 / Example:**
> 路牌为深蓝色金属底板，上面以**清晰醒目的白色无衬线字体**展示文字，**字面平整，为印刷工艺**，表面在夕阳下**微微反光**

---

### 3️⃣ 信息图场景的文字补充 / Text Supplementation for Infographics

**原则 / Principle:**
在信息图/知识类场景中，如果描述只暗示有文字但未给出内容，需要**主动补充简短且明确的实际文案**。

In infographic or knowledge-based scenes, if the description implies text but doesn't provide content, you must **actively supplement concise and explicit actual text content**.

**✅ 正确做法 / Correct:**
- 补充具体文字："垃圾分类小知识"、"厨余垃圾"、"容易腐烂"
- 说明文字布局：标题、分区名称、步骤标识
- 文字与图形一一对应

**❌ 错误做法 / Incorrect:**
- ❌ "列表"（太模糊）
- ❌ "相关内容"（不明确）
- ❌ "搭配文字说明"（不具体）

---

## 文字信息型示例 / Text-Centric Examples

<span id="文字信息型示例-text-centric-examples"></span>

### 示例 1 / Example 1 - 街头路牌

**中文 / Chinese:**

> 一处上海武康路的街头场景，整体为写实摄影风格。画面中央偏左的位置，一块经典的上海道路指示牌固定在粗壮的梧桐树树干上，路牌为深蓝色金属底板，边角略显圆润，上面以清晰醒目的白色无衬线字体横向排列文字，上方为中文**"武康路"**，下方为英文**"WUKANG ROAD"**，中英文对齐规整，字面平整，为印刷工艺，表面在夕阳下微微反光。路牌周围是高大的梧桐树，树干纹理粗粝，枝叶在画面上方形成自然的框景。背景中可见成排老洋房建筑，外立面为米色与浅灰色，带有法式与海派风格的窗框与阳台细节，但整体被刻意虚化，仅保留轮廓与色块。傍晚时分的暖橙色夕阳从画面右后方斜射而来，为树干、路牌边缘和建筑外墙镀上一层柔和金色光晕。前景的柏油路面上散落着几片干燥的落叶，一名行人正骑着自行车从画面右侧经过，人物与自行车同样处于轻微虚化状态，强化街头瞬间感与空间纵深。整体色调温暖而克制，光影柔和，背景虚化明显，营造出浓郁的城市生活气息与富有情绪张力的黄昏氛围。

**English:**

> A street scene on Wukang Road in Shanghai, captured in a realistic photographic style. In the center-left of the frame, a classic Shanghai street sign is fixed to the sturdy trunk of a plane tree. The sign features a dark blue metal base plate with slightly rounded corners, displaying clear and prominent white sans-serif text arranged horizontally, with Chinese characters **"武康路"** on top and English **"WUKANG ROAD"** below, aligned neatly, with smooth surface as printed craftsmanship, slightly reflective under the setting sun. Around the sign are tall plane trees with rough bark textures, their branches and leaves forming a natural framing effect in the upper portion of the frame. In the background, rows of old Western-style houses are visible, with facades in beige and light gray tones, featuring French and Haipai-style window frames and balcony details, but overall intentionally blurred, retaining only contours and color blocks. The warm orange sunset light of late afternoon streams diagonally from the rear right, casting a soft golden halo on the tree trunk, sign edges, and building exterior walls. Several dry fallen leaves are scattered on the asphalt road surface in the foreground, while a cyclist passes through from the right side of the frame, with both the figure and bicycle in slight blur, enhancing the sense of a candid street moment and spatial depth. The overall color palette is warm yet restrained, with soft lighting and noticeably blurred background, creating a rich atmosphere of urban life and emotionally charged twilight mood.

---

### 示例 2 / Example 2 - 知识卡片

**中文 / Chinese:**

> 一幅采用清新水彩风格的手绘垃圾分类知识卡片，背景为米白色纸张质感。画面顶部中央醒目地展示大标题**"垃圾分类小知识"**。主体部分是一个圆形分类结构图，正中央印有文字**"分类让地球更干净"**。圆形结构的上方区域展示厨余垃圾，绘有果皮和剩饭的插图，上方标题为**"厨余垃圾"**，下方说明文字为**"容易腐烂"**，补充知识点为**"可以变成肥料"**。左下角区域展示可回收物，绘有纸张和塑料瓶，标题为**"可回收物"**，说明文字为**"可以再利用"**，补充知识点为**"节约资源"**。右上角区域展示有害垃圾，绘有电池和药品，标题为**"有害垃圾"**，说明文字为**"对环境有危险"**，补充知识点为**"要单独处理"**。右下角区域展示其他垃圾，绘有纸巾和灰尘，标题为**"其他垃圾"**，说明文字为**"不能回收"**，补充知识点为**"要正确投放"**。卡片底部印有总结性标语**"正确分类，从我做起！"**。画面中还包含趣味知识文字**"一个电池能污染一大片土地。"**。整体风格可爱生动，色彩明亮柔和，布局清晰，充满寓教于乐的氛围。

---

### 示例 3 / Example 3 - PPT演示

**中文 / Chinese:**

> 一幅现代商务风格的PPT幻灯片设计，背景采用深邃的黑色基底，表面装饰有精美的金色纹理与元素，整体氛围优雅且富有权威感，色彩对比鲜明，兼具专业感与科技感。画面顶部中央以金色大写字母清晰醒目地展示着主标题**"投资组合多元化策略"**。标题下方使用白色字体呈现了一段简洁的说明文字，内容为**"多元化通过在各种资产类别（包括股票、债券、房地产和新兴市场）之间分配投资来降低风险。平衡的投资组合能在市场波动中适应，并最大化长期回报。"**。画面右侧设置有一个标题为**"资产分配概况"**的堆叠柱形图，图表通过颜色编码清晰地展示了各类别的具体分配比例，具体包括**"股票50%"**、**"债券25%"**、**"房地产15%"**和**"替代选择10%"**，且配有对应的图例，使数据一目了然。图表左侧配有支持性的文字说明：**"通过不同资产减少对单一市场衰退的暴露提高稳定性。"**。底部水平排列着象征不同资产类别的股票市场图标、房屋图标和金币图标，以增强视觉表现力。页脚处用白色小字体注明了**"咨询说明：过去的表现不能说明未来的结果。"**。

---

## 🎨 通用型图像描述要求 / General Image Description Requirements

<span id="通用型图像描述要求-general-image-description-requirements"></span>

当画面不以写实人像或文字为核心，而是以景物、物体、抽象和风格构成为主时：

When the image is not centered on realistic human portraits or text, but instead focuses on scenery, objects, abstraction, or stylistic composition:

### 描述重点 / Description Focus

#### 1️⃣ 视觉主体 / Visual Subjects

**必须描述 / Must Describe:**
- ✅ 主要视觉主体的种类、数量
- ✅ 形态、比例关系与排列方式
- ✅ 颜色、材质、表面细节
- ✅ 前景、中景、背景位置
- ✅ 相互之间的空间关系

**示例 / Example:**
> 画面中央是一张粉色布艺三人沙发，其表面呈现自然的布料肌理与轻微的坐卧褶皱，并搭配两个同色系的方形抱枕；沙发左侧摆放一把绿色绒面单人扶手椅...

---

#### 2️⃣ 光线与色彩 / Lighting and Color

**重点补充 / Emphasize:**
- ✅ **光源方向**：来自哪个方向
- ✅ **光线类型**：自然光 / 人造光
- ✅ **光线特征**：强弱、软硬、冷暖
- ✅ **光效**：阴影、高光、反射、氛围光
- ✅ **色调**：整体色调与局部色彩对比

**示例 / Example:**
> 光线从侧前方照射，形成柔和的光影对比，照亮人物上半身，阴影部分过渡自然。整体色调温暖而克制，色彩饱和度适中

---

#### 3️⃣ 场景类型与尺度 / Scene Type and Scale

**说明 / Specify:**
- ✅ 场景类型（自然景观、城市空间、室内环境、静物摆拍、概念化空间）
- ✅ 时间特征（清晨、黄昏、夜晚）
- ✅ 天气状态（雨后、薄雾、晴朗等）
- ✅ 尺度感（空间大小、物体比例）

---

#### 4️⃣ 情绪与风格 / Emotion and Style

**适度补充 / Moderately Supplement:**
- ✅ 画面传达的情绪（宁静、温暖、神秘、未来感、诗意感）
- ✅ 风格倾向（写实、抽象、极简、奢华等）

---

## 通用型示例 / General Examples

<span id="通用型示例-general-examples"></span>

### 示例 1 / Example 1 - 汽车摄影

**中文 / Chinese:**

> 一辆白色现代品牌的双门轿跑车型，其车身经过低趴改装处理，搭配银色多辐式轻量化轮毂，展现出强烈的运动气息。前脸部分，黑色蜂窝状进气格栅与内部的LED矩阵大灯形成鲜明对比，大灯点亮后呈现出锐利的三角形光源效果；车顶中央位置粘贴有一块红色矩形贴纸，贴纸上清晰可见白色的品牌标识图案。在车辆的右侧，有一棵枝叶繁茂的红棕色松树，树叶因季节变化而呈现出丰富的橙红色调；左侧则立着一根垂直的木质电线杆，底部延伸至画面之外。地面为灰色的柏油铺装路面，表面带有细微的裂缝与磨损痕迹，远处天空呈现出淡蓝色的渐变效果，光线柔和且带有暖黄色的倾向（推测为日出后或日落前的黄金时刻）。整个画面的构图采用了低角度平视的方式，使得车辆成为视觉焦点，背景元素简洁而不喧宾夺主，充分突出了车辆的力量感与精致度。

**English:**

> A white modern brand coupe model, with a lowered stance modification, featuring silver multi-spoke lightweight wheels that exude a strong sense of sportiness. At the front, the black honeycomb grille contrasts sharply with the embedded LED matrix headlights, which when illuminated present a sharp triangular light pattern; a red rectangular decal is affixed to the center of the roof, with a white brand logo clearly visible on it. To the right of the vehicle stands a lush reddish-brown pine tree, its leaves displaying rich orange and red tones due to seasonal changes; to the left rises a vertical wooden utility pole, extending beyond the bottom of the frame. The ground is gray asphalt pavement, with subtle cracks and wear marks on the surface, while the distant sky presents a pale blue gradient effect, with soft light carrying a warm yellow hue (likely the golden hour after sunrise or before sunset). The composition employs a low-angle eye-level perspective, making the vehicle the visual focal point, with background elements that are clean without distracting, fully highlighting the power and sophistication of the vehicle.

---

### 示例 2 / Example 2 - 室内场景

**中文 / Chinese:**

> 一个现代简约风格的客厅空间：画面中央是一张粉色布艺三人沙发，其表面呈现自然的布料肌理与轻微的坐卧褶皱，并搭配两个同色系的方形抱枕；沙发左侧摆放一把绿色绒面单人扶手椅，椅腿采用浅木色细长设计；沙发前方设置一张圆形实木茶几，桌面边缘带有竖条纹雕刻工艺，台面上整齐摆放着一个透明玻璃花瓶（内插3-4枝黄色小花）、一个金属框架小灯笼以及两个圆柱形陶瓷小罐；茶几后方靠近墙面的位置立着一盏三脚木质落地灯，其灯杆呈Y字形分叉结构以支撑白色的布艺灯罩，灯罩边缘呈现自然的垂坠形态；背景墙面采用暖橙色哑光涂料，下半部分则设有白色的护墙板线条，左侧墙面开设一扇带有白色纱帘的窗户，阳光透过纱帘在地面与墙面上形成了斑驳的光影效果；地面铺设着浅灰色的短绒地毯，地毯下方则是鱼骨拼贴的实木地板，整个空间的照明充足且光线分布均匀，色彩的饱和度处于适中水平，整体呈现出真实摄影所特有的质感。

**English:**

> A modern minimalist living room space: in the center of the frame is a pink fabric three-seater sofa, its surface presenting natural fabric texture with slight wrinkling from use, accompanied by two square pillows of the same color series; to the left of the sofa sits a green velvet armchair with slender light-colored wooden legs; in front of the sofa is a round solid wood coffee table, with carved vertical stripe patterns on the edge, on the table surface neatly arranged a transparent glass vase (containing 3-4 small yellow flowers), a small metal-frame lantern, and two cylindrical ceramic jars; behind the coffee table near the wall stands a three-legged wooden floor lamp, its pole featuring a Y-shaped fork structure to support a white fabric lampshade with natural draping at the edges; the background wall is painted with warm orange matte finish, with white wainscoting molding on the lower portion, while the left wall features a window with white sheer curtains through which sunlight filters to create dappled light and shadow effects on the floor and wall; the floor is covered with a light gray short-pile rug over herringbone-patterned solid wood flooring, the entire space is abundantly and evenly lit, color saturation is at a moderate level, overall presenting the authentic textural quality characteristic of realistic photography.

---

## 💡 描述优化技巧 / Description Optimization Techniques

<span id="描述优化技巧-description-optimization-techniques"></span>

### 技巧 1：从抽象到具体 / From Abstract to Concrete

**❌ 过于抽象 / Too Abstract:**
> 一个美丽的场景

**✅ 具体描述 / Specific:**
> 一个阳光明媚的春日清晨，绿色的草地上点缀着黄色和白色的小花，远处的山峦在薄雾中若隐若现

---

### 技巧 2：增强感官细节 / Enhance Sensory Details

**❌ 缺少细节 / Lacking Details:**
> 一个人在吃饭

**✅ 丰富感官 / Rich Sensory:**
> 一位中年男子坐在木制餐桌前，手中拿着筷子夹起一块热气腾腾的红烧肉，食物表面泛着油光，散发出诱人的香气

---

### 技巧 3：明确视觉风格 / Specify Visual Style

**❌ 风格模糊 / Unclear Style:**
> 一幅画

**✅ 风格明确 / Clear Style:**
> 一幅印象派风格的油画作品，笔触粗犷而富有表现力，色彩鲜艳明亮，捕捉了光影在物体表面的瞬间变化

---

### 技巧 4：优化空间关系 / Optimize Spatial Relationships

**❌ 空间混乱 / Confused Space:**
> 桌子、椅子、柜子

**✅ 空间清晰 / Clear Space:**
> 一张圆形木桌放置在房间中央，周围摆放着四把布艺椅子；靠墙位置是一个白色的书柜，柜门半开，露出里面的书籍

---

## ⚠️ 常见错误 / Common Mistakes

<span id="常见错误-common-mistakes"></span>

### 错误 1：使用条列格式 / Using Bullet Point Format

**❌ 错误 / Incorrect:**
> 一个女孩在读书。
> - 年龄：20岁
> - 场景：树下
> - 服装：白色连衣裙

**✅ 正确 / Correct:**
> 一位约20岁的女孩，穿着白色连衣裙，坐在古老的大树下专注地阅读书籍...

---

### 错误 2：添加额外说明 / Adding Extra Commentary

**❌ 错误 / Incorrect:**
> （这是一个人像场景，所以我重点描述人物特征）一个女孩站在窗边...

**✅ 正确 / Correct:**
> 一位年轻女孩站在窗边...

---

### 错误 3：专有名词被翻译 / Proper Nouns Translated

**❌ 错误 / Incorrect:**
> 她穿着**耐克**鞋，手里拿着**苹果15**手机

**✅ 正确 / Correct:**
> 她穿着 **Nike** 鞋，手里拿着 **iPhone 15** 手机

---

### 错误 4：文字未标注 / Text Not Marked

**❌ 错误 / Incorrect:**
> 路牌上写着武康路

**✅ 正确 / Correct:**
> 路牌上以白色字体展示着 **"武康路"**

---

### 错误 5：缺少视觉风格 / Missing Visual Style

**❌ 错误 / Incorrect:**
> 一辆汽车在路上行驶

**✅ 正确 / Correct:**
> 一辆白色轿车在沥青公路上行驶，整体采用写实摄影风格，背景虚化处理...

---

## 📚 总结与最佳实践 / Summary and Best Practices

### ✅ DO's - 推荐做法

1. **自然叙述** - 使用连贯的段落式描述
2. **合理补充** - 适当增加环境、光线、材质信息
3. **详略得当** - 已详尽的仅优化语言，冗余的适当压缩
4. **保留专有名词** - 品牌、人名、IP等原样保留
5. **标注文字内容** - 所有文字用引号标出
6. **明确视觉风格** - 在描述中明确整体风格

### ❌ DON'Ts - 避免做法

1. **❌ 不要使用条列、编号、代码块**
2. **❌ 不要添加额外的说明和注释**
3. **❌ 不要翻译或改写专有名词**
4. **❌ 不要让文字描述与视觉描述混淆**
5. **❌ 不要引入与原描述冲突的新概念**
6. **❌ 不要输出判断过程或类别标注**

---

## 🎯 实战案例 / Practical Examples

### 案例 1：从简单到丰富 / From Simple to Rich

**原始输入 / Original Input:**
> 一个女孩在树下看书

**优化输出 / Optimized Output:**
> 一位约20岁的女孩，穿着白色连衣裙，坐在一棵古老的大树下阅读书籍。她专注地低着头，长发自然垂落在肩头。阳光透过茂密的树叶，在她身上投下斑驳的光影。周围是绿色的草地，远处有安静的小路延伸。整体呈现写实摄影风格，浅景深构图，背景虚化，光线柔和自然。

---

### 案例 2：文字场景优化 / Text Scene Optimization

**原始输入 / Original Input:**
> 一个路牌

**优化输出 / Optimized Output:**
> 一处街道路牌固定在梧桐树树干上，路牌为深蓝色金属底板，边角圆润，上面以清晰醒目的白色无衬线字体横向排列文字，上方为中文**"武康路"**，下方为英文**"WUKANG ROAD"**，字面平整，为印刷工艺，表面在夕阳下微微反光。周围是高大的梧桐树，枝叶形成自然的框景。背景中老洋房建筑被虚化。傍晚暖橙色夕阳从右后方斜射，为路牌镀上金色光晕。整体色调温暖，写实摄影风格。

---

### 案例 3：产品描述优化 / Product Description Optimization

**原始输入 / Original Input:**
> 一个可乐罐

**优化输出 / Optimized Output:**
> 一罐红色铝制可乐罐，表面呈现光滑的金属质感，罐身印有清晰的白色品牌标识。罐体表面覆盖着细密的水珠，在光线下闪烁着晶莹的光泽。几滴冷凝水珠顺着罐壁缓缓滑落，在底部汇聚。罐子放置在深色木质桌面上，与桌面形成鲜明对比。侧方光线照射，形成柔和的高光和阴影，增强立体感。整体采用产品摄影风格，背景虚化，突出主体细节，色彩饱和度适中，呈现清新诱人的质感。

---

<div align="center">

---

**🌟 核心原则总结 / Core Principles Summary:**

1. **自然叙述 / Natural Narrative** - 连贯的段落式描述
2. **视觉完整 / Visual Completeness** - 包含所有关键视觉要素
3. **风格明确 / Clear Style** - 明确整体视觉风格
4. **专有保留 / Preserve Proper Nouns** - 品牌名称等原样保留
5. **文字标注 / Mark Text** - 文字内容用引号标出

**最重要的是：只输出优化后的描述文本！**

**Most importantly: Output ONLY the rewritten description text!**

---

**Made with ❤️ based on [GLM-Image](https://github.com/zai-org/GLM-Image)**

---

*💡 Tip: Press `Home` or `Ctrl + Home` to scroll back to top / 按 `Home` 或 `Ctrl + Home` 返回顶部*

</div>
