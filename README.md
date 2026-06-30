# Lumen Echo

> Listen to your Obsidian notes instead of reading them.
> 把 Obsidian 笔记“听”出来,而不是“看”。

One click on the left ribbon turns the **currently open note** into an audio file,
saved locally in your vault and named after the note. Powered by
[SiliconFlow](https://siliconflow.cn) or [OpenRouter](https://openrouter.ai)
text-to-speech.

点击左侧栏的图标,即可把**当前打开的笔记**生成为一段音频,存到你库里的本地文件夹,
文件名跟笔记名走。语音可由[硅基流动 (SiliconFlow)](https://siliconflow.cn)
或 [OpenRouter](https://openrouter.ai) 提供。

> This is the **release-only** repository (built plugin for distribution).
> 本仓库只用于**发布构建产物**。

---

## English

### Why

Sometimes you want to *hear* a note — on a walk, doing chores, resting your eyes —
not stare at it. Lumen Echo makes that one click away.

### Install via BRAT (recommended for now)

1. Install the **BRAT** plugin from Obsidian Community Plugins.
2. In BRAT settings → **Add Beta plugin** → paste:
   ```
   leoyang1984/lumen-echo-public
   ```
3. Enable **Lumen Echo** under Settings → Community plugins.
4. BRAT will auto-update it when new releases ship.

### Manual install

1. Download `main.js`, `manifest.json`, and `styles.css` from the
   [latest release](https://github.com/leoyang1984/lumen-echo-public/releases/latest).
2. Put them in `<your vault>/.obsidian/plugins/lumen-echo/`.
3. Reload Obsidian and enable **Lumen Echo**.

### Setup

1. Get a SiliconFlow API key from <https://siliconflow.cn> or an OpenRouter key
   from <https://openrouter.ai>.
2. Settings → **Lumen Echo**:
   - **TTS provider** — SiliconFlow or OpenRouter
   - **API key** — your provider key
   - **Model** — SiliconFlow defaults to `FunAudioLLM/CosyVoice2-0.5B`;
     OpenRouter defaults to `google/gemini-3.1-flash-tts-preview`
   - **Voice** — alex / anna / bella / benjamin / charles / claire / david / diana
     for SiliconFlow; `Sulafat` is the OpenRouter Gemini default for warm
     long-form narration
   - **Speed** — 0.25 – 4.0
   - **Storage folder** — where mp3 files go (default `Audio`)
   - **When regenerating** — overwrite / keep one per voice / keep every version

### Use

1. Open a note.
2. Click the **Lumen Echo** icon in the left ribbon, or run the command
   *“Read current note aloud”*.
3. The note's Markdown is cleaned into plain speech, sent to the selected TTS
   provider, and the resulting audio file is saved and opened so you can press play.

### Notes

- Long notes are split into chunks and the audio segments are stitched together.
- Markdown (code blocks, links, images, frontmatter, formatting) is stripped so
  the engine reads only the prose.
- OpenRouter Gemini TTS returns PCM, so Lumen Echo wraps it as a playable `.wav`;
  other providers continue to save `.mp3`.

---

## 中文

### 解决什么问题

有时候你想**听**一篇笔记 —— 走路、做家务、想让眼睛歇会儿 —— 而不是盯着屏幕看。
Lumen Echo 让这件事只需一次点击。

### 通过 BRAT 安装(当前推荐)

1. 在 Obsidian 社区插件里安装 **BRAT** 插件。
2. BRAT 设置 → **Add Beta plugin** → 粘贴:
   ```
   leoyang1984/lumen-echo-public
   ```
3. 在「设置 → 第三方插件」里启用 **Lumen Echo**。
4. 之后有新版本,BRAT 会自动更新。

### 手动安装

1. 从[最新 Release](https://github.com/leoyang1984/lumen-echo-public/releases/latest)
   下载 `main.js`、`manifest.json`、`styles.css`。
2. 放进 `<你的库>/.obsidian/plugins/lumen-echo/`。
3. 重载 Obsidian,启用 **Lumen Echo**。

### 配置

1. 在 <https://siliconflow.cn> 获取 SiliconFlow API key,或在
   <https://openrouter.ai> 获取 OpenRouter key。
2. 设置 → **Lumen Echo**:
   - **TTS provider** —— SiliconFlow 或 OpenRouter
   - **API key** —— 对应服务的密钥
   - **Model** —— SiliconFlow 默认 `FunAudioLLM/CosyVoice2-0.5B`;
     OpenRouter 默认 `google/gemini-3.1-flash-tts-preview`
   - **Voice** —— SiliconFlow 可选 alex / anna / bella / benjamin / charles /
     claire / david / diana; OpenRouter Gemini 默认 `Sulafat`,适合温暖耐听的长文朗读
   - **Speed** —— 语速 0.25 – 4.0
   - **Storage folder** —— 音频存放文件夹(默认 `Audio`)
   - **When regenerating** —— 重新生成时:覆盖 / 每个音色各留一份 / 每次都留

### 使用

1. 打开一篇笔记。
2. 点击左侧栏的 **Lumen Echo** 图标,或运行命令 *“Read current note aloud”*。
3. 笔记会被清洗成纯文本送去合成,生成的音频自动保存并打开,点击即可播放。

### 说明

- 长笔记会自动分段合成并拼接成一个音频。
- Markdown(代码块、链接、图片、YAML 头、格式符号)会被清除,只朗读正文。
- OpenRouter Gemini TTS 返回 PCM,Lumen Echo 会自动封装成可播放的 `.wav`;
  其他服务继续保存为 `.mp3`。

---

## License / 授权

Licensed under the **PolyForm Noncommercial License 1.0.0** — free for
noncommercial use; **commercial use is not permitted**. See [LICENSE](LICENSE).

采用 **PolyForm Noncommercial License 1.0.0** 授权:**仅限非商业用途,禁止商用**。
详见 [LICENSE](LICENSE)。
