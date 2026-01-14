<div align="center">

# 🎨 AI Image & Video Generation Prompting Guide
# 🎨 AI 图像与视频生成提示词指南

**Comprehensive bilingual prompting guides for AI image and video generation tools**

**AI图像与视频生成工具的全面双语提示词指南**

![GitHub repo size](https://img.shields.io/github/repo-size/Yifo98/Prompting-Guide?style=flat-square)
![GitHub language count](https://img.shields.io/github/languages/count/Yifo98/Prompting-Guide?style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/Yifo98/Prompting-Guide?style=flat-square)

</div>

---

## 📑 Table of Contents / 目录

- [🎨 GLM-Image](#glm-image) - Image description optimization / 图像描述优化
- [🎬 LTX-2](#ltx-2) - Production-grade AI video generation / 生产级AI视频生成
- [🎬 通义万相](#通义万相) - Alibaba's AI video generation tool / 阿里巴巴AI视频生成工具

---

<details>
<summary><h3 id="glm-image">🎨 GLM-Image</h3></summary>

> **Source / 来源:**
> This guide is organized from the [GLM-Image](https://github.com/zai-org/GLM-Image) project's prompt optimization system.
>
> **本文档来源:**
> 本指南整理自 [GLM-Image](https://github.com/zai-org/GLM-Image) 项目的提示词优化系统。

---

**Quick Access / 快速访问:** View the complete [GLM-Image Prompting Guide](./GLM-Image.md)

**Overview / 概述:**

GLM-Image is an advanced prompt design system specialized in image description optimization. It transforms raw image descriptions into vivid, visually precise, and generation-friendly prompts with strong visual analysis capabilities and professional bilingual expression.

GLM-Image 是一个专注于图像描述优化的高级提示词设计系统，具备出色的视觉解析能力与双语表达水平，能够将原始图像描述转化为更具画面感、审美价值与生成友好度的提示词。

本指南涵盖了：

- **Universal Principles** - 6 core rules for all image types (natural narrative, reasonable enhancement, proper nouns preservation, text marking, style specification)
- **Image Classification** - Three types: realistic portraits, text-centric, and general images
- **Detailed Requirements** - Complete element checklists for each image type
- **Rich Examples** - 9+ comprehensive examples with Chinese and English translations
- **Best Practices** - Optimization techniques and common mistakes to avoid

本指南涵盖了：

- **通用原则** - 6条适用于所有图像类型的核心规则（自然叙述、合理补充、专有名词保留、文字标注、风格明确）
- **图像分类** - 三种类型：写实人像、文字信息、通用图像
- **详细要求** - 每种图像类型的完整要素清单
- **丰富示例** - 9+个中英文对照的完整示例
- **最佳实践** - 优化技巧和常见错误避免

---

**Key Features / 主要特性:**

✨ **Intelligent Classification** - Automatically categorizes images and applies optimal strategies
✨ **Bilingual Support** - Complete Chinese and English system prompts
✨ **Rich Examples** - Detailed examples for portraits, text scenes, and general images
✨ **Optimization Focus** - Enhances visual appeal without changing original meaning
✨ **Generation-Friendly** - Optimized prompts specifically for AI image generation

✨ **智能分类** - 自动判断图像类型并应用最佳策略
✨ **双语支持** - 完整的中英文系统提示词
✨ **丰富示例** - 人像、文字、通用场景的详细示例
✨ **优化专注** - 提升视觉吸引力而不改变原意
✨ **生成友好** - 专门为AI图像生成优化的提示词

---

**Core Principles / 核心原则:**

1. **Use natural narrative language** - Avoid bullet points or structured formatting
2. **Reasonably supplement visual details** - Enhance lighting, materials, atmosphere when needed
3. **Preserve proper nouns** - Keep brand names, IPs, locations unchanged
4. **Mark text clearly** - Use quotation marks for all text content
5. **Specify visual style** - Clearly state the overall visual style
6. **Output only the description** - No explanations or category labels

1. **使用自然叙述语言** - 避免条列或结构化格式
2. **合理补充视觉细节** - 适当增强光线、材质、氛围
3. **保留专有名词** - 品牌名、IP、地名等保持不变
4. **清晰标注文字** - 所有文字内容用引号标出
5. **明确视觉风格** - 清晰说明整体视觉风格
6. **只输出描述文本** - 不加解释或类别标注

---

**Model Resources / 模型资源:**

- 🤖 [GitHub Repository](https://github.com/zai-org/GLM-Image)
- 📖 [Example Code](https://github.com/zai-org/GLM-Image/blob/main/examples/prompt_utils.py)

---

</details>

---

<details>
<summary><h3 id="ltx-2">🎬 LTX-2</h3></summary>

> **Official Documentation / 官方文档:**
> This guide is based on the official [LTX-2 Prompting Guide](https://ltx.io/model/model-blog/prompting-guide-for-ltx-2). Please visit the official website for the most up-to-date information.
>
> **本文档基于官方文档:**
> 本指南基于官方 [LTX-2 提示词指南](https://ltx.io/model/model-blog/prompting-guide-for-ltx-2)。请访问官方网站获取最新信息。

---

**Quick Access / 快速访问:** View the complete [LTX-2 Prompting Guide](./LTX-2.md)

**Overview / 概述:**

LTX-2 is the first DiT-based audio-video foundation model that contains all core capabilities of modern video generation in one model. Developed by Lightricks, it supports synchronized audio and video generation, high fidelity (up to 4K), multiple performance modes, and production-ready outputs.

LTX-2 是第一个基于DiT的音视频基础模型，在一个模型中包含了现代视频生成的所有核心能力。由Lightricks开发，支持同步音视频生成、高保真度（最高4K）、多种性能模式和可用于生产的输出。

本指南涵盖了：

- **Key Aspects** - What to include in prompts (shot, scene, action, characters, camera, audio)
- **Example Prompts** - 11 detailed examples with English and Chinese translations
- **Best Practices** - Tips for optimal results
- **Technical Terms** - Categories, visual details, sound & voice, camera language
- **What Works Well** - Strengths of LTX-2 (cinematic compositions, emotive moments, atmosphere)
- **What to Avoid** - Common pitfalls and how to avoid them
- **Quick Tips Summary** - DO's and DON'Ts for effective prompting

本指南涵盖了：

- **关键要素** - 提示词应包含的内容（镜头、场景、动作、角色、摄像机、音频）
- **示例提示词** - 11个详细的中英文对照示例
- **最佳实践** - 获取最佳效果的技巧
- **技术术语** - 类别、视觉细节、声音与配音、摄像机语言
- **有效应用** - LTX-2的优势（电影构图、情感时刻、氛围营造）
- **应避免事项** - 常见误区及避免方法
- **快速提示总结** - 有效提示词的推荐做法和避免做法

---

**Key Features / 主要特性:**

✨ **Production-Grade** - Up to 4K resolution at 50 fps with synchronized audio
✨ **Fast Generation** - Designed for real-time video generation workflows
✨ **Open Source** - Available on Hugging Face with Python inference
✨ **Audio-Video Sync** - Native support for synchronized audio and video generation
✨ **Multiple Modes** - Text-to-video, image-to-video, and video-to-video transformations

✨ **生产级质量** - 最高4K分辨率，50fps，支持同步音频
✨ **快速生成** - 专为实时视频生成工作流设计
✨ **开源可用** - 可在Hugging Face上获取，支持Python推理
✨ **音视频同步** - 原生支持同步音视频生成
✨ **多种模式** - 文本生视频、图片生视频、视频生视频转换

---

**Model Resources / 模型资源:**

- 🤖 [Hugging Face Model](https://huggingface.co/Lightricks/LTX-2)
- 📖 [GitHub Repository](https://github.com/Lightricks/LTX-2)
- 🎮 [Online Playground](https://app.ltx.studio/ltx-2-playground/t2v)
- 📝 [Official Documentation](https://docs.ltx.video)

---

</details>

---

<details>
<summary><h3 id="通义万相">🎬 通义万相 (Wanxiang AI Video)</h3></summary>

> **Official Documentation / 官方文档:**
> This guide is based on the official [通义万相 AI生视频使用指南](https://alidocs.dingtalk.com/i/nodes/jb9Y4gmKWrx9eo4dCql9LlbYJGXn6lpz) (Wanxiang AI Video Generation User Guide). Please visit the official website for the most up-to-date information.
>
> **本文档基于官方文档:**
> 本指南基于官方 [通义万相AI生视频使用指南](https://alidocs.dingtalk.com/i/nodes/jb9Y4gmKWrx9eo4dCql9LlbYJGXn6lpz)。请访问官方网站获取最新信息。

---

**Quick Access / 快速访问:** View the complete [通义万相 Prompting Guide](./通义万相.md)

**Overview / 概述:**

通义万相AI生视频是阿里巴巴推出的AI视频生成工具，支持通过文字描述生成高质量视频内容。本指南涵盖了：

- 基础篇：产品介绍、6种提示词公式（基础、进阶、图生视频、声音、参考生视频、多镜头）、视频声音生成
- 进阶篇：电影美学控制（光源、光照类型、时段、景别、构图、摄像机、色调）、动态控制（运动、情绪、镜头运动）
- 风格篇：视觉风格、特效与风格化
- 附录：最佳实践、常见错误、总结

通义万相 AI Video Generation is Alibaba's AI video generation tool that supports generating high-quality video content from text descriptions. This guide covers:

- **Basics**: Product introduction, 6 prompt formulas (basic, advanced, image-to-video, audio, reference video, multi-shot), video audio generation
- **Advanced**: Cinematic aesthetics control (light sources, lighting types, time of day, shot size, composition, camera, color tone), dynamic control (movement, emotions, camera movements)
- **Styles**: Visual styles, special effects, and stylization
- **Appendix**: Best practices, common errors, summary

---

**Key Features / 主要特性:**

✨ **中文友好** - 专门优化的中文提示词支持
✨ **场景丰富** - 支持人物、风景、城市等多种场景
✨ **风格多样** - 写实、动漫、电影等多种艺术风格
✨ **声音生成** - 支持人声、音效、环境音、背景音乐
✨ **参考功能** - 支持图片和参考视频生成
✨ **易于上手** - 清晰的公式和模板，快速入门

✨ **Chinese-optimized** - Specially optimized Chinese prompt support
✨ **Rich Scenes** - Supports various scenes like characters, landscapes, cities
✨ **Diverse Styles** - Multiple artistic styles including realistic, anime, cinematic
✨ **Audio Generation** - Supports human voice, sound effects, ambient sounds, background music
✨ **Reference Features** - Supports image and reference video generation
✨ **Easy to Learn** - Clear formulas and templates for quick start

---

**Platform Resources / 平台资源:**

- 🌐 [Official Website](https://wanxiang.aliyun.com/)
- 📖 [Official Documentation](https://alidocs.dingtalk.com/i/nodes/jb9Y4gmKWrx9eo4dCql9LlbYJGXn6lpz)
- 🎨 [Online Platform](https://wanxiang.aliyun.com/)

---

</details>

---

<div align="center">

**🌟 Star this repository if you find it helpful!**

**如果这个仓库对你有帮助，请给个Star支持一下！**

---

**Made with ❤️ for personal use by [Yifo98](https://github.com/Yifo98)**

---

*💡 Tip: Press `Home` or `Ctrl + Home` to scroll back to top / 按 `Home` 或 `Ctrl + Home` 返回顶部*

*💡 Tip: Click on "View the complete guide" links to access full documentation / 点击"查看完整指南"链接访问完整文档*

</div>
