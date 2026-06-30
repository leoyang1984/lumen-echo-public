## Lumen Echo 0.0.2

This release adds OpenRouter TTS support alongside the existing SiliconFlow
backend, making it easier to compare voices and providers for note narration.

### Highlights

- Added a TTS provider switch: SiliconFlow or OpenRouter.
- Added OpenRouter text-to-speech models, with
  `google/gemini-3.1-flash-tts-preview` as the default model.
- Set Gemini's default voice to `Sulafat`, a warm voice suited for longer
  article-style narration.
- Added model-specific OpenRouter voice options, including Grok Voice,
  Gemini TTS, Kokoro, Zonos, Orpheus, Sesame, Mistral Voxtral, and MAI-Voice.
- Fixed Gemini TTS output handling on OpenRouter: Gemini only supports PCM, so
  Lumen Echo now wraps that output as a playable `.wav` file.

### Notes

- SiliconFlow output continues to save as `.mp3`.
- OpenRouter Gemini TTS output saves as `.wav`.
- The Speed setting currently applies to SiliconFlow. OpenRouter TTS model
  support for speed is inconsistent, so it is not sent for OpenRouter requests.

## 中文说明

这个版本在原有硅基流动 TTS 之外,新增了 OpenRouter TTS 适配,方便在不同服务和音色之间切换测试。

### 主要更新

- 增加 TTS provider 切换:SiliconFlow / OpenRouter。
- 增加 OpenRouter TTS 模型列表,默认模型为
  `google/gemini-3.1-flash-tts-preview`。
- 将 Gemini 默认音色设为 `Sulafat`,更适合温暖、耐听的长文朗读。
- 增加 OpenRouter 各模型对应的音色选项。
- 修复 OpenRouter Gemini TTS 只支持 PCM 的问题:现在会自动封装为可播放的
  `.wav` 文件。

### 说明

- SiliconFlow 仍保存为 `.mp3`。
- OpenRouter Gemini TTS 保存为 `.wav`。
- Speed 设置目前只应用于 SiliconFlow;OpenRouter 各模型对语速支持不一致,暂不发送。
