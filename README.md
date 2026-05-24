<div align="center">

<img src="Screenshots/offlinellm.png" width="800" />

**The first of its kind — a fully offline, private AI chat app for Android**

The only Android LLM app that literally cannot phone home. All LLM inference runs on-device via llama.cpp. No internet. No cloud. No tracking.

[![Kotlin](https://img.shields.io/badge/Kotlin-2.3-111111.svg?logo=kotlin&logoColor=white&color=bfff00)](https://kotlinlang.org)
[![Android](https://img.shields.io/badge/Android-14%2B-111111.svg?logo=android&logoColor=white&color=bfff00)](https://developer.android.com)
[![Version](https://img.shields.io/badge/Version-5.0.1-111111.svg?color=bfff00)](https://github.com/jegly/OfflineLLM/releases)
[![License](https://img.shields.io/badge/License-Apache%202.0-111111.svg?color=bfff00)](LICENSE)
[![llama.cpp](https://img.shields.io/badge/llama.cpp-GGUF-111111.svg?color=bfff00)](https://github.com/ggerganov/llama.cpp)
[![Offline](https://img.shields.io/badge/Network-Zero%20Permissions-111111.svg?color=bfff00)]()
[![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-Material%203-111111.svg?logo=jetpackcompose&logoColor=white&color=bfff00)](https://developer.android.com/jetpack/compose)
![GitHub all releases](https://img.shields.io/github/downloads/jegly/OfflineLLM/total?color=bfff00)
[![HuggingFace](https://img.shields.io/badge/🤗%20HuggingFace-Releases-111111.svg?color=bfff00)](https://huggingface.co/jegly)

[![Download APK](https://img.shields.io/badge/Download_APK-111111?style=for-the-badge&logo=android&logoColor=white&color=bfff00)](https://github.com/jegly/OfflineLLM/releases/latest)

<a href="https://www.buymeacoffee.com/jegly">
  <img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png"
       alt="Buy Me A Coffee"
       height="41"
       width="174"
       style="filter: hue-rotate(80deg) saturate(1.8);">
</a>

</div>

If this project helped you, please ⭐️ star it. **Also try [Box](https://github.com/jegly/Box)** — a full-stack on-device AI app built on the same philosophy.

<details>
<summary><b>📱 Screenshots</b></summary>

<p align="center">
<img src="Screenshots/Welcome_to_OfflineLLM.jpg" width="400" />
<img src="Screenshots/Choose_assistant.jpg" width="400" />
<img src="Screenshots/Conversation_preview.jpg" width="400" />
<img src="Screenshots/Settings_preview.jpg" width="400" />
</p>

<p align="center">
<img src="Screenshots/Settings_preview_2.jpg" width="400" />
<img src="Screenshots/Application_about_section.jpg" width="400" />
</p>

</details>

## Features

- **100% Offline** — no INTERNET permission in the manifest, cannot phone home
- **On-Device Inference** — GGUF models via llama.cpp with ARM NEON/SVE/i8mm
- **Streaming Responses** — ~25 tok/s on budget devices, 40–60+ on flagships
- **Import Any Model** — bring your own GGUF at runtime via file picker
- **Multiple Conversations** — auto-titled, renameable, searchable
- **Translator** — 75+ languages
- **Advanced Sampling** — Temperature, Top-P, Top-K, Min-P, Repeat Penalty
- **System Prompts** — General, Coder, Creative Writer, Tutor, Translator
- **Markdown + TTS** — formatted responses, read aloud via system TTS
- **Thinking Tag Stripping** — hides `<think>` blocks from reasoning models
- **Theming** — System / Light / Dark / AMOLED + 9 accent colours
- **Security** — encrypted settings, optional biometric lock, secure file deletion
- **Chat Backup** — export/import as JSON
- **Gemma 4** — automatic prompt template detection

## Install

v5.0.1 ships in three flavours:

| Release | Bundled Model | APK Size | Best For |
|---|---|---|---|
| **Vanilla** | None (bring your own) | Small | Users with their own GGUF model |
| **Qwen3.5 0.8B** | Qwen3.5 0.8B Q4_K_M | ~600 MB | Everyday use, 4–6 GB RAM |
| **Gemma4-E2B** | Gemma4-E2B-it Q4_K_M | ~1.4 GB | Best quality, 6–8 GB RAM — [HuggingFace download](https://huggingface.co/jegly/OfflineLLM_V5.0.1_Signed_Release_Gemma4_E2B_IT.apk/blob/main/OfflineLLM_V5.0.1_Signed_Release_Gemma4_E2B_IT.apk) |

> Gemma4-E2B is hosted on HuggingFace due to GitHub's 2 GB file limit. All releases are identical in features.

1. Download from [Releases](https://github.com/jegly/OfflineLLM/releases)
2. **Settings → Apps → Install unknown apps** → allow your file manager
3. Open the APK, tap Install, complete onboarding

Or via ADB:

```bash
adb install OfflineLLM_V5.0.1.apk
```

<details>
<summary><b>Checksums</b></summary>

- **Vanilla** — SHA-256 `3c6c89e0c4aa95fd1acd68070a295a9011faa235c786ad2f4648149a26f67305`
- **Qwen3.5 Release** — SHA-256 `839a795da2b1c85d27f3f29fbb1189d6935227ad905ad60d689ff6e5dfcf3205`
- **Gemma4 Release** — Xet hash `69945c715660e1dcb098ee4db0157d783038db819d50043859a9fe099b75b1f7`

</details>

## Recommended Models

| Model (Q4_K_M) | Approx. Size | RAM Required / Best For |
| :--- | :--- | :--- |
| **gemma-3-270m-it-qat-Q4_K_M.gguf** | ~300 MB | 2–4 GB RAM devices, fast responses |
| **Qwen3.5 0.8B Q4_K_M** | ~530 MB | Good balance for 4–6 GB RAM |
| **gemma-4-E2B-it-GGUF** (2.3B effective) | ~1.3 GB | **Recommended for 6–8 GB RAM** |
| **gemma-4-E4B-it-GGUF** (4.5B effective) | ~2.5 GB | **Recommended for 8 GB RAM** |
| **Qwen3.5 4B Q4_K_M** | ~2.5 GB | Flagship (12 GB+ RAM) |

Search the model name + "GGUF" on [HuggingFace](https://huggingface.co). `Q4_K_M` is the best quality/speed balance.

## Performance

| Device Tier | RAM | Expected Speed |
|---|---|---|
| Budget (ZTE, etc.) | 4 GB | ~25 tok/s with 270M model |
| Mid-range (Pixel 7) | 6–8 GB | 30–50 tok/s with 1B model |
| Flagship (Pixel 10 Pro) | 12–16 GB | 40–60+ tok/s with 4B model |

## Build from Source

**Prerequisites:** JDK 17, Android SDK (compileSdk 37), NDK r27, CMake 3.22.1

```bash
git clone --recurse-submodules https://github.com/jegly/OfflineLLM.git
cd OfflineLLM

# Optional: bundle a model in the APK
cp /path/to/model.gguf app/src/main/assets/model/

./gradlew assembleDebug
```

First build compiles llama.cpp from source (~15–20 min). Subsequent builds are fast.

<details>
<summary><b>Project structure</b></summary>

- **`smollm/`** — Native llama.cpp JNI module
  - `src/main/cpp/` — C++ inference engine + JNI bridge
  - `src/main/java/` — SmolLM.kt, GGUFReader.kt wrappers
- **`app/`** — Main Android application (`src/main/java/com/jegly/offlineLLM/`)
  - `ai/` — InferenceEngine, ModelManager, SystemPrompts
  - `data/` — Room database, DAOs, repositories
  - `di/` — Hilt dependency injection modules
  - `ui/` — Compose screens, components, theme, navigation
  - `utils/` — BiometricHelper, MemoryMonitor, SecurityUtils, TTS
- **`llama.cpp/`** — git submodule

</details>

## Security & Privacy

- Zero network permissions (no INTERNET, no ACCESS_NETWORK_STATE)
- No Google Play Services or Firebase dependencies
- Encrypted settings via Jetpack Security
- Optional biometric lock
- Memory Tagging Extension enabled (`memtagMode="sync"`)
- Secure deletion — files overwritten before removal
- No logging of prompts or responses

## License

Apache License 2.0. llama.cpp backend: MIT. Native wrapper adapted from [SmolChat-Android](https://github.com/shubham0204/SmolChat-Android) (Apache 2.0).

---

<div align="center">

**[www.jegly.xyz](https://www.jegly.xyz)**

</div>
