# Prompting Guide for LTX-2
# LTX-2 提示词指南

> **Official Documentation / 官方文档:**
> This guide is based on the official [LTX-2 Prompting Guide](https://ltx.io/model/model-blog/prompting-guide-for-ltx-2). Please visit the official website for the most up-to-date information.
>
> **本文档基于官方文档:**
> 本指南基于官方 [LTX-2 提示词指南](https://ltx.io/model/model-blog/prompting-guide-for-ltx-2)。请访问官方网站获取最新信息。

---

To get the most out of the LTX-2 model, a good prompt will make all the difference. The key is painting a complete picture of the story you're telling that flows naturally from beginning to end, covering all the elements the model needs to bring your vision to life.

要充分利用 LTX-2 模型,一个好的提示词至关重要。关键是要完整地描绘你要讲述的故事,从头到尾自然流畅地展开,涵盖模型实现你的愿景所需的所有元素。

---

## Key Aspects to Include
## 应包含的关键方面

- **Establish the shot.** Use cinematography terms that match your preferred film genre. Include aspects like scale or specific category characteristics to further refine the style you're looking for.

**确定镜头。** 使用与你偏好的电影类型相匹配的摄影术语。加入规模或特定类别特征等方面,进一步完善你想要的风格。

- **Set the scene.** Describe lighting conditions, color palette, surface textures, and atmosphere to shape the mood.

**设定场景。** 描述光线条件、色彩调色板、表面纹理和氛围,以塑造氛围。

- **Describe the action.** Write the core action as a natural sequence, flowing from beginning to end.

**描述动作。** 把核心动作写成一个自然的顺序,从头到尾顺畅。

- **Define your character(s).** Include age, hairstyle, clothing, and distinguishing details. Express emotions through physical cues.

**定义角色。** 包括年龄、发型、服装和显著细节。通过身体信号表达情感。

- **Identify camera movement(s).** Specify when the view should shift and how. Including how subjects or objects appear after the camera motion gives the model a better idea of how to finish the motion.

**识别摄像机运动。** 具体说明视角何时以及如何切换。包括摄像机运动后主体或物体的呈现方式,能让模型更好地完成动作。

- **Describe the audio.** Use clear descriptions for ambient sounds, music, audio, and speech. For dialogue, place the text between quotation marks and (if required) mention the language and accent you would like the character to have.

**描述音频。** 使用清晰的环境音、音乐、音频和语音描述。对于对话,将文本置于引号之间,并(如有需要)注明你希望角色拥有的语言和口音。

---

## Example Prompts
## 示例提示词

### Example 1
### 示例 1

**English Prompt:**

> An action packed, cinematic shot of a monster truck driving fast towards the camera, the truck passes the cameras it pans left to follow the trucks reckless drive. dust and motion blur is around the truck, hand held feel to the camera as it tries to track its ride into the distance. the truck then drifts and turns around, then drives back towards the camera until seen in extreme close up.

**中文翻译:**

> 这是一辆充满动作、电影感十足的镜头,一辆怪兽卡车高速驶向镜头,卡车左转,跟随卡车鲁莽的驾驶。尘埃和运动模糊环绕着卡车,手持镜头捕捉着它试图远离的感觉。卡车随后漂移并掉头,然后驶回摄像头,直到出现极近距离。

---

### Example 2
### 示例 2

**English Prompt:**

> A warm sunny backyard. The camera starts in a tight cinematic close-up of a woman and a man in their 30s, facing each other with serious expressions. The woman, emotional and dramatic, says softly, "That's it... Dad's lost it. And we've lost Dad."
>
> The man exhales, slightly annoyed: "Stop being so dramatic, Jess."
>
> A beat. He glances aside, then mutters defensively, "He's just having fun."
>
> The camera slowly pans right, revealing the grandfather in the garden wearing enormous butterfly wings, waving his arms in the air like he's trying to take off.
>
> He shouts, "Wheeeew!" as he flaps his wings with full commitment.
>
> The woman covers her face, on the verge of tears. The tone is deadpan, absurd, and quietly tragic.

**中文翻译:**

> 一个温暖阳光明媚的后院。镜头从一个紧凑的电影特写开始,展现一对三十多岁的男女面对面,表情严肃。那位情绪激动且戏剧化的女子轻声说:"就这样......爸爸疯了。而且我们失去了爸爸。"
>
> 那人呼出一口气,略显恼怒:"别这么戏剧化了,杰斯。"
>
> 停顿。他瞥了一眼,然后防备地嘟囔道:"他只是玩得开心。"
>
> 镜头缓缓向右拉,露出花园里的祖父,他长着巨大的蝴蝶翅膀,挥舞着双臂,仿佛想要起飞。
>
> 他一边全力拍动翅膀,一边喊道:"哇——!"
>
> 那女人捂住脸,眼眶湿润。语气冷淡、荒诞且低调悲剧。

---

### Example 3
### 示例 3

**English Prompt:**

> INT. OVEN – DAY. Static camera from inside the oven, looking outward through the slightly fogged glass door. Warm golden light glows around freshly baked cookies. The baker's face fills the frame, eyes wide with focus, his breath fogging the glass as he leans in. Subtle reflections move across the glass as steam rises.
>
> Baker (whispering dramatically): "Today… I achieve perfection."
>
> He leans even closer, nose nearly touching the glass.
>
> "Golden edges. Soft center. The gods themselves will smell these cookies and weep."
>
> Baker: "Wait—"
>
> (beat)
>
> "Did I… forget the chocolate chips?"
>
> Cut to side view — coworker pops into frame, chewing casually.
>
> Coworker (mouth full): "Nope. You forgot the sugar."
>
> Quick zoom back to the baker's horrified face, pressed against the oven door, as cookies deflate behind the glass. Steam drifts upward in slow motion.
>
> pixar style acting and timing

**中文翻译:**

> 内景。烤箱——白天。烤箱内部的静态摄像头,透过略微起雾的玻璃门向外拍摄。温暖的金色光芒环绕着刚出炉的饼干。面包师的脸庞充满了画面,眼睛睁得大大的,专注而睁大,呼吸在玻璃上形成雾气,他俯身靠近。随着蒸汽上升,玻璃上会有细微的反射。
>
> 贝克(戏剧性地低声):"今天......我追求完美。"
>
> 他更靠近,鼻子几乎碰到玻璃。
>
> "金色边缘。软心。连神明都会闻到这些饼干,哭泣。"
>
> 贝克:"等等——"
>
> (节拍)
>
> "我......忘了巧克力豆?"
>
> 侧面切换——同事突然出现在画面中,悠闲地咀嚼着。
>
> 同事(嘴里含着东西):"没有。你忘了加糖。"
>
> 快速拉近面包师那张惊恐的脸,贴着烤箱门,饼干在玻璃后瘪了。蒸汽缓慢上升。
>
> 皮克斯风格的表演与节奏

---

## For Best Results
## 为了获得最佳效果

- Keep your prompt in a single flowing paragraph to give the model a cohesive scene to work with.

将提示保持在一个流畅的段落中,为模型提供一个连贯的场景。

- Use present tense verbs to describe movement and action.

使用现在时动词来描述动作和动作。

- Match your detail to the shot scale. Closeups need more precise detail than wide shots.

把细节和镜头比例匹配。特写镜头需要比广角更精细的细节。

- When describing camera movement, focus on the camera's relationship to the subject.

描述相机运动时,应关注相机与主体的关系。

- You should expect to write 4 to 8 descriptive sentences to cover all the key aspects of the prompt.

你应该预计写4到8个描述性句子,以涵盖提示的所有关键方面。

- Don't be afraid to iterate! LTX-2 is designed for fast experimentation, so refining your prompt is part of the workflow.

不要害怕不断迭代!LTX-2 设计为快速实验,因此完善提示词是工作流程的一部分。

---

### Example 4
### 示例 4

**English Prompt:**

> NT. DAYTIME TALK SHOW SET – AFTERNOON
>
> Soft studio lighting glows across a warm-toned set. The audience murmurs faintly as the camera pans to reveal three guests seated on a couch — a middle-aged couple and the show's host sitting across from them.
>
> The host leans forward, voice steady but probing:
>
> Host: "When did you first notice that your daughter, Missy, started to spiral?"
>
> The woman's face crumples; she takes a shaky breath and begins to cry. Her husband places a comforting hand on her shoulder, looking down before turning back toward the host.
>
> Father (quietly, with guilt): "We… we don't know what we did wrong."
>
> The studio falls silent for a moment. The camera cuts to the host, who looks gravely into the lens.
>
> Host (to camera): "Let's take a look at a short piece our team prepared — chronicling Missy's downward path."
>
> The lights dim slightly as the camera pushes in on the mother's tear-streaked face. The studio monitors flicker to life, beginning to play the segment as the audience holds its breath.

**中文翻译:**

> 北领地。白天脱口秀节目安排——下午
>
> 柔和的演播室灯光洒在暖色调的布景上。当镜头扫开,露出三位坐在沙发上的嘉宾时,观众轻声低语——一对中年夫妇和对面的主持人。
>
> 主持人身体前倾,声音平稳却带着探询:
>
> 主持人:"你是什么时候第一次注意到你女儿米西开始陷入低谷的?"
>
> 女人的脸垮了;她颤抖着吸了口气,开始哭泣。她的丈夫安慰地把手放在她肩上,低头看着她,然后转回头看向主人。
>
> 父亲(低声,带着愧疚):"我们......我们不知道自己哪里做错了。"
>
> 演播室里一片寂静。镜头切换到主持人,他严肃地望着镜头。
>
> 主持人(对镜头):"让我们来看看我们团队准备的一段短片——记录 Missy 的堕落之路。"
>
> 随着镜头拉近母亲泪痕斑斑的脸,灯光微微暗暗。演播室监听器闪烁着亮起,开始播放该片段,观众屏住呼吸。

---

## Additional Helpful Terms
## 额外有用术语

This is not an exhaustive list. Use it to give you some examples of how to craft the result you're looking for.

这并不是一个详尽的列表。用它给你一些示例,教你如何打造你想要的效果。

### Categories
### 类别

**Animation:** stop-motion, 2D/3D animation, claymation, hand-drawn

**动画:** 定格动画、2D/3D 动画、黏土动画、手绘

---

### Example 5
### 示例 5

**English Prompt:**

> Pinocchio is sitting in an interrogation room, looking nervous, and slightly sweating. He's saying very quietly to himself "I didn't do it... I didn't do it... I'm not a murderer". Pinocchio's nose is quickly getting longer and longer. The camera is zooming in on the double sided mirror in the back of the room, The mirror is turning black as the camera approaches it, and exposes a blurry silhouette of two FBI detectives who stand in the dark lit room on the other side. One of them is saying "I'm telling you, I have a feeling something is off with this kiddo"

**中文翻译:**

> 匹诺曹坐在审讯室里,看起来紧张,微微出汗。他很轻声地对自己说:"我没做......不是我干的。。。我不是杀人犯。"匹诺曹的鼻子越来越长。镜头拉近房间后方的双面镜子,镜子变黑,镜头靠近时映出两名 FBI 侦探的模糊身影,他们站在另一侧昏暗的房间里。其中一个说:"我跟你说,我感觉这孩子有点不对劲"

---

**Stylized:** comic book, cyberpunk, 8-bit pixel, surreal, minimalist, painterly, illustrated

**风格化:** 漫画书、赛博朋克、8 位像素、超现实、极简、画风、插画

---

### Example 6
### 示例 6

**English Prompt:**

> The young african american woman wearing a futuristic transparent visor and a bodysuit with a tube attached to her neck. she is soldering a robotic arm. she stops and looks to her right as she hears a suspicious strong hit sound from a distance. she gets up slowly from her chair and says with an angry african american accent: "Rick I told you to close that goddamn door after you!". then, a futuristic blue alien explorer with dreadlocks wearing a rugged outfit walks into the scene excitedly holding a futuristic device and says with a low robotic voice: "Fuck the door look what I found!". the alien hands the woman the device, she looks down at it excitedly as the camera zooms in on her intrigued illuminated face. she then says: "is this what I think it is?" she smiles excitedly. sci-fi style cinematic scene

**中文翻译:**

> 这位年轻的非裔美国女性戴着未来感十足的透明面罩,穿着脖子上连接管子的连体衣。她正在焊接机械臂。她停下脚步,向右看去,听到远处传来一声可疑的强烈击打声。她慢慢从椅子上站起来,带着愤怒的非裔美国口音说:"里克,我告诉过你,你先把那该死的门关上!"然后,一位留着脏辫、穿着粗犷服装的未来蓝色外星探险者兴奋地走进场景,手持一个未来装置,低沉机械地说:"去他妈的门,看看我找到了什么!"外星人把装置递给那位女士,她兴奋地低头看着它,镜头拉近她那张好奇、发光的脸。她接着说:"这是我想的那个吗?"她兴奋地笑着。科幻风格电影场景

---

**Cinematic:** period drama, film noir, fantasy, epic space opera, thriller, modern romance, experimental film, arthouse, documentary

**电影类:** 时代剧、黑色电影、奇幻、史诗太空歌剧、惊悚、现代爱情、实验电影、艺术电影、纪录片

---

### Example 7
### 示例 7

**English Prompt:**

> Cinematic action packed shot. the man says silently: "We need to run." the camera zooms in on his mouth then immediately screams: "NOW!". the camera zooms back out, he turns around, and starts running away, the camera tracks his run in hand held style. the camera cranes up and show him run into the distance down the street at a busy New York night.

**中文翻译:**

> 电影般的动作镜头。那人默默地说:"我们得跑。"镜头拉近他的嘴巴,然后立刻喊道:"现在!"镜头拉远,他转身开始逃跑,镜头以手持方式跟踪他的奔跑。镜头拉高,拍到他在纽约繁忙夜晚的街道上跑向远方。

---

### Visual Details
### 视觉细节

- **Lighting conditions:** flickering candles, neon glow, natural sunlight, dramatic shadows

**光线条件:** 摇曳的蜡烛、霓虹灯光、自然阳光、戏剧性的阴影

- **Textures:** rough stone, smooth metal, worn fabric, glossy surfaces

**质地:** 粗糙的石头、光滑的金属、磨损的织物、光亮的表面

- **Color palette:** vibrant, muted, monochromatic, high contrast

**色彩调色板:** 鲜艳、柔和、单色调、高对比度

- **Atmospheric elements:** fog, rain, dust, particles, smoke

**大气元素:** 雾、雨、尘埃、颗粒、烟雾

---

### Example 8
### 示例 8

**English Prompt:**

> The camera opens in a calm, sunlit frog yoga studio. Warm morning light washes over the wooden floor as incense smoke drifts lazily in the air. The senior frog instructor sits cross-legged at the center, eyes closed, voice deep and calm. "We are one with the pond." All the frogs answer softly: "Ommm..." "We are one with the mud." "Ommm..." He smiles faintly. "We are one with the flies." A quiet pause.
>
> The camera slowly pans to the side — one frog twitches, eyes darting. Suddenly — *thwip!* — its tongue snaps out, catching a fly mid-air and pulling it into its mouth. The master exhales slowly, still serene.
>
> "But we do not chase the flies…"
>
> Beat. "…not during class." The guilty frog freezes, then lowers its head in visible shame, folding its hands back into the meditative pose. The other frogs resume their chant: "Ommm..." Camera holds for a moment on the embarrassed frog, eyes closed too tightly, pretending nothing happened.

**中文翻译:**

> 镜头开场时,是一个宁静、阳光明媚的青蛙瑜伽馆。温暖的晨光洒在木地板上,香烟懒洋洋地飘散在空气中。这位高级青蛙教练盘腿坐在中央,闭着眼睛,声音低沉而平静。"我们与池塘合而为一。"所有青蛙都轻声回答:"嗯......""我们与泥土融为一体。""嗯......"他微微一笑。"我们与苍蝇合而为一。"一阵安静的停顿。
>
> 镜头缓缓侧移——一只青蛙抽搐,眼睛四处游移。突然——*嗖!*——它的舌头猛地伸出,抓住空中的一只苍蝇,把它拉进嘴里。大师缓缓呼出一口气,依旧平静。
>
> "但我们不追苍蝇......"
>
> 停顿。"......上课时不行。"那只内疚的青蛙僵住了,随后低下头,明显羞愧,双手重新交叠成冥想的姿势。其他青蛙继续唱着:"嗯......"镜头停留在那只尴尬的青蛙身上,眼睛紧闭,假装什么都没发生。

---

### Sound and Voice
### 声音与配音

- **Setting:** Ambient coffeeshop noises, dripping rain and wind blowing, forest ambience with birds singing

**场景:** 咖啡馆环境音,滴水雨声和风声,森林氛围中鸟鸣

- **Dialogue style:** Energetic announcer, resonant voice with gravitas, distorted radio-style, robotic monotone, childlike curiosity

**对话风格:** 充满活力的播音员,声音洪亮且庄重,失真广播风格,机械单调,孩童般的好奇心

- **Volume:** quiet whisper, mutters, shouts, screams

**音量:** 轻声耳语,低语,喊叫,尖叫

---

### Example 9
### 示例 9

**English Prompt:**

> A warm, intimate cinematic performance inside a cozy, wood-paneled bar, lit with soft amber practical lights and shallow depth of field that creates glowing bokeh in the background. The shot opens in a medium close-up on a young female singer in her 20s with short brown hair and bangs, singing into a microphone while strumming an acoustic guitar, her eyes closed and posture relaxed. The camera slowly arcs left around her, keeping her face and mic in sharp focus as two male band members playing guitars remain softly blurred behind her. Warm light wraps around her face and hair as framed photos and wooden walls drift past in the background. Ambient live music fills the space, led by her clear vocals over gentle acoustic strumming.

**中文翻译:**

> 一场温暖而亲密的电影表演,发生在一个温馨的木质镶板酒吧内,柔和的琥珀色实用灯光和浅景深营造出背景散景的光辉。镜头以中特写开场,一位二十多岁的年轻女歌手,短棕发留刘海,闭着眼睛,姿态放松,一边弹着木吉他,一边对着麦克风唱歌。镜头缓缓绕着她左转,保持她的脸和麦克风清晰对焦,身后两名男乐队成员弹吉他,画面模糊。温暖的光线环绕着她的脸和头发,背景中飘过装框的照片和木质墙壁。氛围现场音乐充满了空间,由她清晰的嗓音引领,伴随着轻柔的原声扫弦。

---

### Technical Style Markers
### 技术风格标记

- **Camera language:** follows, tracks, pans across, circles around, tilts upward, pushes in, pulls back, overhead view, handheld movement, over-the-shoulder, wide establishing shot, static frame

**摄像机语言:** 跟随、跟踪、横移、绕圈、向上倾斜、推近、拉回、俯视、手持移动、肩膀后移、广角建立镜头、静态画面

- **Film characteristics:** jittery stop-motion, pixelated edges, lens flares, film grain

**胶片特性:** 抖动的定格动画、像素化的边缘、镜头光晕、胶片颗粒

- **Scale indicators:** expansive, epic, intimate, claustrophobic

**尺度指标:** 广阔、史诗、亲密、幽闭恐惧

- **Pacing and temporal effects:** slow motion, time-lapse, rapid cuts, lingering shot, continuous shot, freeze-frame, fade-in, fade-out, seamless transition, dynamic movement, sudden stop

**节奏与时间效果:** 慢动作、延时、快速剪辑、持续镜头、连续镜头、定格、淡入淡出、无缝过渡、动态移动、突然停止

- **Specific visual effects (if relevant):** particle systems, motion blur, depth of field

**具体视觉效果(如相关):** 粒子系统、运动模糊、景深

---

### Example 10
### 示例 10

**English Prompt:**

> An animated cinematic shot. a robot, walks slowly, the camera dollys back and keep the robots slow walk in a medium shot. the robot start running slowly and heavily. it then stops, and the camera keeps dollying back, until a blue similiar robot appears in an over the shoulder shot.

**中文翻译:**

> 一个动画电影镜头。一个机器人缓慢走着,摄像机推车后退,保持机器人缓慢走路的中景。机器人开始缓慢而沉重地奔跑。随后画面停下,摄像机不断往后移动,直到一个蓝色类似机器人出现在肩膀后方的镜头中。

---

## What Works Well with LTX-2
## LTX-2 的良好应用

> **Cinematic compositions:**
> Wide, medium, and close-up shots with thoughtful lighting, shallow depth of field, and natural motion.

> **电影作品:**
> 广角、中景和特写镜头,配合用心的光线、浅景深和自然运动。

> **Emotive human moments:**
> LTX-2 excels at single-subject emotional expressions, subtle gestures, and facial nuance.

> **感人至深的人性时刻:**
> LTX-2 擅长单一主题的情感表达、细微的动作和面部表情细腻。

> **Atmosphere & setting:**
> Weather effects like fog, mist, golden hour light, soft shadows, rain, reflections, and ambient textures all help ground the scene.

> **氛围与环境:**
> 天气效果如雾、雾、黄金时光、柔和阴影、雨水、倒影和环境纹理都帮助场景扎根。

> **Clean, readable camera language:**
> Clear directions like "slow dolly in," "handheld tracking," or "over-the-shoulder" improve consistency.

> **清晰易读的相机语言:**
> 像"慢速推车进"、"手持追踪"或"肩上移动"这样清晰的指示,可以提升一致性。

> **Stylized aesthetics:**
> Painterly, noir, analog film look, fashion editorial, pixelated animation, or surreal art styles work especially well when named early in the prompt.

> **风格化美学:**
> 画家风格、黑色电影风格、时尚编辑风格、像素动画或超现实艺术风格在提示开头就特别合适。

> **Lighting and mood control:**
> Backlighting, color palettes, soft rim light, flickering lamps — these anchor tone better than generic mood words.

> **灯光与情绪控制:**
> 背光、色彩调色板、柔和的边缘光、闪烁的灯光——这些锚点比普通的情绪词汇更能营造出主色调。

> **Voice:**
> Characters can talk and sing in various languages.

> **配音:**
> 角色可以用多种语言说话和唱歌。

---

### Example 11
### 示例 11

**English Prompt:**

> EXT. SMALL TOWN STREET – MORNING – LIVE NEWS BROADCAST
>
> The shot opens on a news reporter standing in front of a row of cordoned-off cars, yellow caution tape fluttering behind him. The light is warm, early sun reflecting off the camera lens. The faint hum of chatter and distant drilling fills the air.
>
> The reporter, composed but visibly excited, looks directly into the camera, microphone in hand.
>
> Reporter (live):
> "Thank you, Sylvia. And yes — this is a sentence I never thought I'd say on live television — but this morning, here in the quiet town of New Castle, Vermont… black gold has been found!"
>
> He gestures slightly toward the field behind him.
>
> Reporter (grinning):
> "If my cameraman can pan over, you'll see what all the excitement's about."
>
> The camera pans right, slowly revealing a construction site surrounded by workers in hard hats. A beat of silence — then, with a sudden roar, a geyser of oil erupts from the ground, blasting upward in a violent plume.
>
> Workers cheer and scramble, the black stream glistening in the morning light. The camera shakes slightly, trying to stay focused through the chaos.
>
> Reporter (off-screen, shouting over the noise):
> "There it is, folks — the moment New Castle will never forget!"
>
> The camera catches the sunlight gleaming off the oil mist before pulling back, revealing the entire scene — the small-town skyline silhouetted against the wild fountain of oil.

**中文翻译:**

> 延伸 小镇街 – 早间 – 现场新闻播报
>
> 镜头开场是一位新闻记者站在一排被封锁的汽车前,身后飘动着黄色警戒线。光线温暖,清晨的阳光反射在相机镜头上。空气中弥漫着微弱的交谈声和远处钻孔声。
>
> 记者镇定却明显兴奋,直视镜头,手持麦克风。
>
> 记者(现场):
> "谢谢你,西尔维娅。是的——这是我从没想过会在直播电视上说的一句话——但今天早上,在佛蒙特州这个宁静的小镇新堡......黑金被发现了!"
>
> 他微微指向身后的田野。
>
> 记者(笑着):
> "如果我的摄影师能拉近镜头,你就能明白这场激动到底是什么。"
>
> 镜头向右缓缓移动,露出一个建筑工地,周围是戴着安全帽的工人。一阵寂静——随后,伴随着一声轰鸣,一股油泉从地面喷涌而出,猛烈地喷涌而上。
>
> 工人们欢呼着,奔跑着,黑色的溪流在晨光中闪闪发光。摄像机微微颤抖,试图在混乱中保持聚焦。
>
> 记者(画外音,在嘈杂声中大声喊叫):
> "就是这里,朋友们——纽卡斯尔永远不会忘记的时刻!"
>
> 镜头捕捉到阳光映照在油雾上,随后拉远,展现出整个场景——小镇天际线在狂野的油泉中剪影。

---

## What to Avoid with LTX-2
## 使用 LTX-2 应避免的事项

> **Internal states:**
> Avoid emotional labels like "sad" or "confused" without describing visual cues. Use posture, gesture, and facial expression instead.

> **内部状态:**
> 避免用"悲伤"或"困惑"等情绪标签,但不要描述视觉上的线索。而是通过姿势、手势和面部表情来应对。

> **Text and logos:**
> LTX-2 does not currently generate readable or consistent text. Avoid signage, brand names, or printed material.

> **文字与标志:**
> LTX-2 目前无法生成可读或一致的文本。避免使用标识、品牌或印刷品。

> **Complex physics or chaotic motion:**
> Non-linear or fast-twisting motion (e.g., jumping, juggling) can lead to artifacts or glitches. However, dancing can work well.

> **复杂物理或混沌运动:**
> 非线性或快速扭转运动(如跳跃、杂耍)可能导致伪影或故障。不过,跳舞其实很有效。

> **Scene complexity overload:**
> Too many characters, layered actions, or excessive objects reduce clarity and model accuracy.

> **场景复杂度过载:**
> 字符过多、分层动作或过多的物体会降低清晰度和模型的准确性。

> **Inconsistent lighting logic:**
> Avoid mixing conflicting light sources (e.g., "a warm sunset with cold fluorescent glow") unless clearly motivated.

> **光照逻辑不一致:**
> 除非有明确的动机,否则避免混合冲突的光源(例如"温暖的夕阳配冷的荧光灯")。

> **Over complicated prompts:**
> The more actions/ characters/ instructions you add, the higher the chance some of them won't be seen in the output. Begin with simple things and layer on additional instructions as you iterate.

> **过于复杂的提示:**
> 你添加的动作/字符/指令越多,输出中看到的几率就越大。从简单的事情开始,随着迭代逐步增加额外的指令。

---

## Quick Tips Summary
## 快速提示总结

**DO's (推荐做法):**
- Write 4-8 descriptive sentences in a single paragraph
- Use present tense verbs
- Match detail level to shot scale
- Include clear camera movement directions
- Describe lighting, textures, and atmosphere
- Specify audio and dialogue with quotes

**DON'Ts (避免做法):**
- Use emotional labels without visual cues
- Include text or logos
- Describe complex physics or chaotic motion
- Overload with too many characters/actions
- Mix conflicting light sources
- Overcomplicate prompts

---

*This guide is based on the official LTX-2 documentation and is designed to help you create effective prompts for AI video generation.*

*本指南基于官方 LTX-2 文档,旨在帮助您创建有效的 AI 视频生成提示词。*
