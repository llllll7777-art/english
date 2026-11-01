# english

专四（TEM-4）口语思辨陪练 Skill。对 AI 说 **「我要学英语」** 即可唤醒，开始一轮一轮的英文思辨对话训练。

## 1. 项目解决什么问题

很多备考专四、想提升口语的人，说英语时总带着「中式英语」（Chinese English）：

- **中文直译语序**：把中文语序直接搬到英文（如 "I think study is good"）；
- **中式搭配**：按中文习惯组词（如 "know more about society"、"record teacher point"）；
- **逻辑断层**：观点之间缺少衔接，因果关系不清晰；
- **母语负迁移**：用错冠词、单复数、主谓一致等，一开口就是"汉式英语"。

本项目把这些口语问题做成一轮轮**可反复练习的思辨对话**：AI 出话题和参考句型引导你开口，再逐字转写你的原句、给出一版更地道的优化句并点明问题所在，帮你**边练观点表达、边纠正中式英语**，同时养成一正一反两面论证的思辨习惯。

## 2. 主要功能

- **逐轮出题**：每轮给出一个英文思辨 **Topic**（社会、教育、科技、环境、工作等）+ 一正一反两句英文 **Reference Sentences**，等你口头作答。
- **原句转写**：把你的口述英文原样转写为【我的原句】，保留原始表达。
- **优化改写**：仅给 1 版专四口语级别的【优化句】，优先修正中式英语（拒绝浅层同义词替换），改动核心用**加粗**标出，适配口头表达。
- **简短点评**：【简短点评】点明本次中式英语问题，并说明逻辑、句式、用词的地道度。
- **分支推进**：反馈后提供【继续】（同话题深度追问）和【重新回答】（不换话题重新作答循环）。
- **纯对话训练**：无需脚本、网页抓取、PDF 或图形界面。

## 3. 安装方法

本 Skill 是一个标准的开源 Skill 文件夹，随你的 Agent（豆包办公等支持 Skill 的环境）使用。安装只需把 `english/` 整个文件夹放进 Agent 的**用户 Skill 目录**（通常是以 `.user_skills` 结尾的目录，即 Agent 会扫描并加载 Skill 的位置）：

```
english/
├── SKILL.md            # Skill 核心指令（角色、逐轮流程、分支、输出格式）
├── agents/
│   └── openai.yaml     # 界面元信息与默认提示词
└── README.md           # 本文件（项目根目录）
```

安装后无需任何额外依赖或脚本，Agent 会按 `SKILL.md` 中的描述识别并加载本 Skill。

## 4. 使用方法

1. 对 AI 说 **「我要学英语」**（或"练习专四口语思辨"）唤醒本 Skill。
2. AI 每轮给出：
   - **Topic**：一个英文思辨话题；
   - **Reference Sentences**：一句肯定立场（Agree）、一句否定立场（Disagree）的英文参考句型。
3. 你**口头作答**（打字或语音均可）。
4. AI 输出三块反馈：**①【我的原句】** → **②【优化句】** → **③【简短点评】**。
5. 反馈后二选一：
   - **【继续】**：AI 基于当前话题深度追问，进入同话题的新一轮；
   - **【重新回答】**：不换话题，你重新作答，AI 再次转写、优化、点评，循环到你选【继续】为止。

## 5. 输入输出示例

**AI 出题（输入侧）**

```
Topic: Should college students take a gap year before starting university?

Reference Sentences:
- Agree: A gap year can give students a chance to explore the world before they settle into the routine of academic life.
- Disagree: A gap year may break the habit of study and make it harder for students to pick up where they left off.
```

**你的作答**

```
I think gap year is good because student can relax and know more about society, and then they study more harder.
```

**AI 反馈（输出侧）**

```
①【我的原句】I think gap year is good because student can relax and know more about society, and then they study more harder.

②【优化句】I believe a gap year is worthwhile, because it lets students **take a break from exams and see more of society**, which **may motivate them to study harder** when they return.

③【简短点评】「I think gap year is good」是典型中文直译语序，缺冠词且名词直接当形容词；「know more about society」搭配偏中式。优化句补足逻辑衔接（先放松→后更投入），用 worthwhile 替换泛化 good，改为主从结构更符合口语层次。

【继续】【重新回答】
```

## 局限

- 不支持网页抓取、PDF 处理、图形界面，仅用于对话式口语训练。
