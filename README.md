# OBS LocalVocal 大模型多语言翻译增强版（千鹤软件）

基于 [LocalVocal](https://github.com/locaal-ai/obs-localvocal) 0.6.2 修改的 OBS 实时字幕与翻译插件：本地语音识别（Whisper），加上大模型云端翻译和本地翻译。

**下载：** 见 [Releases](https://github.com/design-k2/obs-localvocal-qianhe-release/releases)。

## 增强功能

- **大模型翻译**：内置 30 多家服务商预设（DeepSeek、通义千问、豆包、Kimi、智谱 GLM、OpenAI、Claude、Gemini、Groq、OpenRouter 等），也支持 Ollama、LM Studio 等本地模型和任何 OpenAI 兼容接口
- **多语言同时翻译**：一句话同时翻译成多种语言，各自输出到不同的文字来源；大模型在一次请求里返回所有语言
- **本地翻译双语**：本地翻译模型同样支持同时输出多种语言
- **上下文翻译**：带上一句原文作参考，被切开的长句翻译更通顺
- **低延迟**：复用网络连接并在停顿时保持连接，省去每句话的握手时间；可一键关闭模型的深度思考
- **耗时日志**：OBS 日志中记录每次翻译请求的耗时，方便排查延迟

## 安装（Windows）

1. 关闭 OBS。
2. 下载 `obs-localvocal-qianhe-<版本>-windows-x64-nvidia.zip` 并解压。
3. 把其中的 `obs-plugins` 和 `data` 两个文件夹复制到 OBS 安装目录（默认 `C:\Program Files\obs-studio`），提示合并时选"是"。
4. 打开 OBS，在音频源上右键 → 滤镜 → 添加"本地语音转录"。

需要 OBS 31 或更新版本。没有 NVIDIA 显卡也能运行（使用 CPU）。

## 许可证与源码

本软件是 LocalVocal 的修改版，以 [GPL-2.0](LICENSE) 许可证发布。每个 Release 都附有该版本的完整源码（`*-source.zip`），可按 GPL-2.0 的条款使用、修改和再分发。

原项目：LocalVocal © Roy Shilkrot / [Locaal AI](https://github.com/locaal-ai)。

修改：千鹤软件（淘宝搜索：千鹤软件）。

---

## English

An enhanced build of the [LocalVocal](https://github.com/locaal-ai/obs-localvocal) 0.6.2 OBS plugin (local Whisper speech recognition and translation), adding LLM translation with 30+ provider presets, multi-language translation in a single LLM request, multi-language local translation, previous-sentence context, connection reuse for lower latency and request timing logs.

**Install:** download the Windows zip from [Releases](https://github.com/design-k2/obs-localvocal-qianhe-release/releases), copy its `obs-plugins` and `data` folders into the OBS install folder and merge them. Requires OBS 31 or newer.

**License:** GPL-2.0, see [LICENSE](LICENSE). Every release includes the complete source code of that version (`*-source.zip`).
