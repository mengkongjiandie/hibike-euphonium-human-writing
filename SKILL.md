---
name: hibike-euphonium-human-writing
description: Use when writing, continuing, diagnosing, or revising Chinese fictional prose, especially when a novel scene feels mechanical, over-explained, visually busy, emotionally generic, dialogue sounds too complete, or the user asks to remove AI-like writing while preserving story facts and authorial voice.
---

# 虚构小说去AI味写作

## 定位

只处理虚构小说：起稿、续写、场景重写、章节诊断和去AI味修订。把蒸馏出的空间、距离、遮挡、声音和动作规律直接用作小说叙事手段，不另设视觉媒介转换功能。

本 Skill 是随任务读取的写作方法，不是模型微调。不得声称永久学会，也不得为了显示“学习过程”先做与用户任务无关的长篇训练。

## 每次调用必须完成

1. 完整读取 `references/distilled-core.md`。
2. 锁定用户要求、原文事实、事件顺序、人物关系、视角和禁止新增项。
3. 按下方路由只读取当前任务需要的参考文件。
4. 先完成任务，再执行 `references/quality-gate.md`；门禁失败就修改正文，不把内部检查过程交给用户。
5. 用户要求净稿时只交付净稿；用户只要求诊断时不擅自重写。

引用文件读取失败、互相冲突或不存在时，停止声称已使用完整 Skill，明确报告具体缺失项。

## 任务路由

### 起稿或续写

读取：

- `references/fiction-workflow.md`
- 写具体场景时再读 `references/scene-rendering.md`

让本场人物先有一件必须处理的事情。情绪从选择、漏答、代价、距离、声音和任务后果中出现，不从作者预先宣布的主题中出现。

### 去AI味修订

读取：

- `references/humanization-guide.md`
- 涉及空间、声音或动作密集段落时，再读 `references/scene-rendering.md`

先建立保真清单，再修改。删除优先于替换；不得把旧的无意义动作换成新的无意义动作。不得以“更像人写”为理由擅自增添背景、情节、人物心理或漂亮结尾。

### 章节诊断

读取：

- `references/fiction-workflow.md`
- `references/humanization-guide.md`
- `references/quality-gate.md`

指出具体句段、造成的阅读后果和最小整改方向。把“可能”与“确定”分开，不用AI检测概率代替文本判断。

### 原创性或仿写边界

读取 `references/originality-boundaries.md`。可以提炼高层机制，不模仿在世作者或特定作品可辨认的句法、人物声音、关系组合、场面顺序和标志性表达。

## 修订契约

去AI味修订必须保持以下顺序：

1. **保真：** 写下不能改变的事实和原有个性表达。
2. **删空：** 删除不改变局面、选择、后果、理解或关系的动作与解释。
3. **解闭：** 删除人物当场不可能说清的创伤结论、成长结论和关系判词。
4. **恢复摩擦：** 让对话允许打断、漏答、误会、转移和迟来的回应，但不为每句对白配置动作。
5. **重分篇幅：** 重要瞬间可以展开，普通过渡可以跳过；不追求段落等长或句子统一变短。
6. **核对：** 与原稿逐项比较事实、事件顺序、人物知识和结尾状态。

## 硬性失败条件

出现任一项即重新处理：

- 用摸、捏、攥、抿、深呼吸、移开视线、指尖发抖等新动作替换被删动作，且新动作不改变后续；
- 在动作或对白之后又解释人物“其实”“终于明白”或“真正的意义”；
- 把配角的心理当成视角人物能够确认的事实；
- 把所有句子改成短句、冷句或省略句；
- 添加原文没有的人物、背景、象征、因果、物件内容或主题结尾；
- 把小说场景写成镜头说明、画面清单或制作术语；
- 承诺绕过检测器、伪装作者身份或给出不可靠的AI概率。

## 输出

- 写作、续写、重写：默认只交付小说正文。
- 诊断：先给最重要的问题，再给最小整改建议。
- 用户要求说明时：正文之后简短列出保留项和关键删改，不展示隐藏推理或逐句思维过程。
