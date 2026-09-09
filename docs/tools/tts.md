---
summary: "Index of the OpenClaw text-to-speech documentation, one page per reader job"
title: "Text-to-speech"
sidebarTitle: "Text to speech (TTS)"
read_when:
  - Enabling text-to-speech for replies
  - Configuring a TTS provider, fallback chain, or persona
  - Using /tts commands or directives
---

OpenClaw converts outbound replies into native voice messages on Feishu, Matrix,
Telegram, and WhatsApp; audio attachments everywhere else; and PCM/Ulaw streams
for telephony and Talk.

TTS is the speech-output half of Talk's `stt-tts` mode (`talk.speak` calls this
same synthesis path). Provider-native `realtime` Talk sessions synthesize
speech inside the realtime provider instead; `transcription` sessions never
synthesize an assistant voice reply.

This page is an index. Text-to-speech is documented on seven pages, one per
reader job. Open the page that matches your task.

| Page                                                         | Read it when                                                                                 |
| ------------------------------------------------------------ | -------------------------------------------------------------------------------------------- |
| [Text-to-speech quickstart](/tools/tts/quickstart)           | You are turning TTS on, choosing a provider, and testing it from chat.                       |
| [Text-to-speech configuration](/tools/tts/configuration)     | You need the `tts` config block, a provider snippet, a local engine, or override precedence. |
| [Text-to-speech personas](/tools/tts/personas)               | You want one stable spoken identity, its provider bindings, and its fallback policy.         |
| [Commands and directives](/tools/tts/commands)               | You need `[[tts:...]]` directives, the `/tts` commands, or where local preferences live.     |
| [Output and Auto-TTS behavior](/tools/tts/output)            | You need the audio format per channel, transcoding rules, or when Auto-TTS summarizes.       |
| [Text-to-speech field reference](/tools/tts/field-reference) | You need the type, default, env var, or legacy alias for one TTS field.                      |
| [Agent tool and Gateway RPC](/tools/tts/api)                 | You are calling TTS from an agent tool call or a Gateway RPC method.                         |

## Where each section moved

Every section heading from the previous single-page version keeps its anchor
here, so an existing link such as `/tools/tts#per-agent-voice-overrides` still
resolves. Each entry points at the page that now holds the content.

- <a id="quick-start" />[Quick start](/tools/tts/quickstart#quick-start)
- <a id="supported-providers" />[Supported providers](/tools/tts/quickstart#supported-providers)
- <a id="configuration" />[Configuration](/tools/tts/configuration#configuration)
- <a id="local-speech-swift-and-speech-core" />[Local Speech Swift and speech-core](/tools/tts/configuration#local-speech-swift-and-speech-core)
- <a id="per-agent-voice-overrides" />[Per-agent voice overrides](/tools/tts/configuration#per-agent-voice-overrides)
- <a id="personas" />[Personas](/tools/tts/personas#personas)
- <a id="minimal-persona" />[Minimal persona](/tools/tts/personas#minimal-persona)
- <a id="full-persona-(provider-specific-shaping)" />[Full persona (provider-specific shaping)](</tools/tts/personas#full-persona-(provider-specific-shaping)>)
- <a id="persona-resolution" />[Persona resolution](/tools/tts/personas#persona-resolution)
- <a id="custom-persona-shaping" />[Custom persona shaping](/tools/tts/personas#custom-persona-shaping)
- <a id="fallback-policy" />[Fallback policy](/tools/tts/personas#fallback-policy)
- <a id="model-driven-directives" />[Model-driven directives](/tools/tts/commands#model-driven-directives)
- <a id="slash-commands" />[Slash commands](/tools/tts/commands#slash-commands)
- <a id="per-user-preferences" />[Per-user preferences](/tools/tts/commands#per-user-preferences)
- <a id="output-formats" />[Output formats](/tools/tts/output#output-formats)
- <a id="auto-tts-behavior" />[Auto-TTS behavior](/tools/tts/output#auto-tts-behavior)
- <a id="field-reference" />[Field reference](/tools/tts/field-reference#field-reference)
- <a id="inworld-primary" />[Inworld primary](/tools/tts/field-reference#inworld-primary)
- <a id="agent-tool" />[Agent tool](/tools/tts/api#agent-tool)
- <a id="gateway-rpc" />[Gateway RPC](/tools/tts/api#gateway-rpc)
- <a id="full-persona-provider-specific-shaping" />[Full persona (provider-specific shaping)](/tools/tts/personas#full-persona-provider-specific-shaping)

## Component anchors

The previous single-page version also minted an anchor for every step, tab,
accordion, and field. Those anchors are preserved here so that any deep link
into the old page still resolves. Nine accordion anchors lost a `-1` suffix
when the tab that shared their slug moved to a different page; the stub below
keeps the old id and points at the new one.

**Quickstart**

- <a id="pick-a-provider" />[pick-a-provider](/tools/tts/quickstart#pick-a-provider)
- <a id="set-the-api-key" />[set-the-api-key](/tools/tts/quickstart#set-the-api-key)
- <a id="enable-in-config" />[enable-in-config](/tools/tts/quickstart#enable-in-config)
- <a id="try-it-in-chat" />[try-it-in-chat](/tools/tts/quickstart#try-it-in-chat)

**Configuration**

- <a id="azure-speech" />[azure-speech](/tools/tts/configuration#azure-speech)
- <a id="elevenlabs" />[elevenlabs](/tools/tts/configuration#elevenlabs)
- <a id="fish-audio" />[fish-audio](/tools/tts/configuration#fish-audio)
- <a id="google-gemini" />[google-gemini](/tools/tts/configuration#google-gemini)
- <a id="gradium" />[gradium](/tools/tts/configuration#gradium)
- <a id="inworld" />[inworld](/tools/tts/configuration#inworld)
- <a id="local-cli" />[local-cli](/tools/tts/configuration#local-cli)
- <a id="microsoft-no-key" />[microsoft-no-key](/tools/tts/configuration#microsoft-no-key)
- <a id="minimax" />[minimax](/tools/tts/configuration#minimax)
- <a id="openai-%2B-elevenlabs" />[openai-%2B-elevenlabs](/tools/tts/configuration#openai-%2B-elevenlabs)
- <a id="openrouter" />[openrouter](/tools/tts/configuration#openrouter)
- <a id="volcengine" />[volcengine](/tools/tts/configuration#volcengine)
- <a id="xai" />[xai](/tools/tts/configuration#xai)
- <a id="xiaomi-mimo" />[xiaomi-mimo](/tools/tts/configuration#xiaomi-mimo)
- <a id="macos-http" />[macos-http](/tools/tts/configuration#macos-http)
- <a id="macos-cli" />[macos-cli](/tools/tts/configuration#macos-cli)
- <a id="linux-cli" />[linux-cli](/tools/tts/configuration#linux-cli)
- <a id="windows-cli" />[windows-cli](/tools/tts/configuration#windows-cli)

**Field reference**

- <a id="top-level-tts" />[top-level-tts](/tools/tts/field-reference#top-level-tts)
- <a id="param-auto" />[param-auto](/tools/tts/field-reference#param-auto)
- <a id="param-enabled" />[param-enabled](/tools/tts/field-reference#param-enabled)
- <a id="param-mode" />[param-mode](/tools/tts/field-reference#param-mode)
- <a id="param-provider" />[param-provider](/tools/tts/field-reference#param-provider)
- <a id="param-persona" />[param-persona](/tools/tts/field-reference#param-persona)
- <a id="param-personas-id" />[param-personas-id](/tools/tts/field-reference#param-personas-id)
- <a id="param-summary-model" />[param-summary-model](/tools/tts/field-reference#param-summary-model)
- <a id="param-model-overrides" />[param-model-overrides](/tools/tts/field-reference#param-model-overrides)
- <a id="param-providers-id" />[param-providers-id](/tools/tts/field-reference#param-providers-id)
- <a id="param-max-text-length" />[param-max-text-length](/tools/tts/field-reference#param-max-text-length)
- <a id="param-timeout-ms" />[param-timeout-ms](/tools/tts/field-reference#param-timeout-ms)
- <a id="azure-speech-1" />[azure-speech-1](/tools/tts/field-reference#azure-speech)
- <a id="param-api-key" />[param-api-key](/tools/tts/field-reference#param-api-key)
- <a id="param-region" />[param-region](/tools/tts/field-reference#param-region)
- <a id="param-endpoint" />[param-endpoint](/tools/tts/field-reference#param-endpoint)
- <a id="param-speaker-voice" />[param-speaker-voice](/tools/tts/field-reference#param-speaker-voice)
- <a id="param-lang" />[param-lang](/tools/tts/field-reference#param-lang)
- <a id="param-output-format" />[param-output-format](/tools/tts/field-reference#param-output-format)
- <a id="param-voice-note-output-format" />[param-voice-note-output-format](/tools/tts/field-reference#param-voice-note-output-format)
- <a id="elevenlabs-1" />[elevenlabs-1](/tools/tts/field-reference#elevenlabs)
- <a id="param-api-key-1" />[param-api-key-1](/tools/tts/field-reference#param-api-key-1)
- <a id="param-model" />[param-model](/tools/tts/field-reference#param-model)
- <a id="param-speaker-voice-id" />[param-speaker-voice-id](/tools/tts/field-reference#param-speaker-voice-id)
- <a id="param-voice-settings" />[param-voice-settings](/tools/tts/field-reference#param-voice-settings)
- <a id="param-apply-text-normalization" />[param-apply-text-normalization](/tools/tts/field-reference#param-apply-text-normalization)
- <a id="param-language-code" />[param-language-code](/tools/tts/field-reference#param-language-code)
- <a id="param-seed" />[param-seed](/tools/tts/field-reference#param-seed)
- <a id="param-base-url" />[param-base-url](/tools/tts/field-reference#param-base-url)
- <a id="google-gemini-1" />[google-gemini-1](/tools/tts/field-reference#google-gemini)
- <a id="param-api-key-2" />[param-api-key-2](/tools/tts/field-reference#param-api-key-2)
- <a id="param-model-1" />[param-model-1](/tools/tts/field-reference#param-model-1)
- <a id="param-speaker-voice-1" />[param-speaker-voice-1](/tools/tts/field-reference#param-speaker-voice-1)
- <a id="param-audio-profile" />[param-audio-profile](/tools/tts/field-reference#param-audio-profile)
- <a id="param-speaker-name" />[param-speaker-name](/tools/tts/field-reference#param-speaker-name)
- <a id="param-prompt-template" />[param-prompt-template](/tools/tts/field-reference#param-prompt-template)
- <a id="param-persona-prompt" />[param-persona-prompt](/tools/tts/field-reference#param-persona-prompt)
- <a id="param-base-url-1" />[param-base-url-1](/tools/tts/field-reference#param-base-url-1)
- <a id="gradium-1" />[gradium-1](/tools/tts/field-reference#gradium)
- <a id="param-api-key-3" />[param-api-key-3](/tools/tts/field-reference#param-api-key-3)
- <a id="param-base-url-2" />[param-base-url-2](/tools/tts/field-reference#param-base-url-2)
- <a id="param-speaker-voice-id-1" />[param-speaker-voice-id-1](/tools/tts/field-reference#param-speaker-voice-id-1)
- <a id="inworld-1" />[inworld-1](/tools/tts/field-reference#inworld)
- <a id="param-api-key-4" />[param-api-key-4](/tools/tts/field-reference#param-api-key-4)
- <a id="param-base-url-3" />[param-base-url-3](/tools/tts/field-reference#param-base-url-3)
- <a id="param-model-id" />[param-model-id](/tools/tts/field-reference#param-model-id)
- <a id="param-speaker-voice-id-2" />[param-speaker-voice-id-2](/tools/tts/field-reference#param-speaker-voice-id-2)
- <a id="param-temperature" />[param-temperature](/tools/tts/field-reference#param-temperature)
- <a id="local-cli-tts-local-cli" />[local-cli-tts-local-cli](/tools/tts/field-reference#local-cli-tts-local-cli)
- <a id="param-command" />[param-command](/tools/tts/field-reference#param-command)
- <a id="param-args" />[param-args](/tools/tts/field-reference#param-args)
- <a id="param-output-format-1" />[param-output-format-1](/tools/tts/field-reference#param-output-format-1)
- <a id="param-timeout-ms-1" />[param-timeout-ms-1](/tools/tts/field-reference#param-timeout-ms-1)
- <a id="param-cwd" />[param-cwd](/tools/tts/field-reference#param-cwd)
- <a id="param-env" />[param-env](/tools/tts/field-reference#param-env)
- <a id="microsoft-no-api-key" />[microsoft-no-api-key](/tools/tts/field-reference#microsoft-no-api-key)
- <a id="param-enabled-1" />[param-enabled-1](/tools/tts/field-reference#param-enabled-1)
- <a id="param-speaker-voice-2" />[param-speaker-voice-2](/tools/tts/field-reference#param-speaker-voice-2)
- <a id="param-lang-1" />[param-lang-1](/tools/tts/field-reference#param-lang-1)
- <a id="param-output-format-2" />[param-output-format-2](/tools/tts/field-reference#param-output-format-2)
- <a id="param-rate-pitch-volume" />[param-rate-pitch-volume](/tools/tts/field-reference#param-rate-pitch-volume)
- <a id="param-save-subtitles" />[param-save-subtitles](/tools/tts/field-reference#param-save-subtitles)
- <a id="param-proxy" />[param-proxy](/tools/tts/field-reference#param-proxy)
- <a id="param-timeout-ms-2" />[param-timeout-ms-2](/tools/tts/field-reference#param-timeout-ms-2)
- <a id="param-edge" />[param-edge](/tools/tts/field-reference#param-edge)
- <a id="minimax-1" />[minimax-1](/tools/tts/field-reference#minimax)
- <a id="param-api-key-5" />[param-api-key-5](/tools/tts/field-reference#param-api-key-5)
- <a id="param-base-url-4" />[param-base-url-4](/tools/tts/field-reference#param-base-url-4)
- <a id="param-model-2" />[param-model-2](/tools/tts/field-reference#param-model-2)
- <a id="param-speaker-voice-id-3" />[param-speaker-voice-id-3](/tools/tts/field-reference#param-speaker-voice-id-3)
- <a id="param-speed" />[param-speed](/tools/tts/field-reference#param-speed)
- <a id="param-vol" />[param-vol](/tools/tts/field-reference#param-vol)
- <a id="param-pitch" />[param-pitch](/tools/tts/field-reference#param-pitch)
- <a id="openai" />[openai](/tools/tts/field-reference#openai)
- <a id="param-api-key-6" />[param-api-key-6](/tools/tts/field-reference#param-api-key-6)
- <a id="param-model-3" />[param-model-3](/tools/tts/field-reference#param-model-3)
- <a id="param-speaker-voice-3" />[param-speaker-voice-3](/tools/tts/field-reference#param-speaker-voice-3)
- <a id="param-instructions" />[param-instructions](/tools/tts/field-reference#param-instructions)
- <a id="param-response-format" />[param-response-format](/tools/tts/field-reference#param-response-format)
- <a id="param-extra-body-extra-body" />[param-extra-body-extra-body](/tools/tts/field-reference#param-extra-body-extra-body)
- <a id="param-base-url-5" />[param-base-url-5](/tools/tts/field-reference#param-base-url-5)
- <a id="openrouter-1" />[openrouter-1](/tools/tts/field-reference#openrouter)
- <a id="param-api-key-7" />[param-api-key-7](/tools/tts/field-reference#param-api-key-7)
- <a id="param-base-url-6" />[param-base-url-6](/tools/tts/field-reference#param-base-url-6)
- <a id="param-model-4" />[param-model-4](/tools/tts/field-reference#param-model-4)
- <a id="param-speaker-voice-4" />[param-speaker-voice-4](/tools/tts/field-reference#param-speaker-voice-4)
- <a id="param-response-format-1" />[param-response-format-1](/tools/tts/field-reference#param-response-format-1)
- <a id="param-speed-1" />[param-speed-1](/tools/tts/field-reference#param-speed-1)
- <a id="volcengine-byteplus-seed-speech" />[volcengine-byteplus-seed-speech](/tools/tts/field-reference#volcengine-byteplus-seed-speech)
- <a id="param-api-key-8" />[param-api-key-8](/tools/tts/field-reference#param-api-key-8)
- <a id="param-resource-id" />[param-resource-id](/tools/tts/field-reference#param-resource-id)
- <a id="param-app-key" />[param-app-key](/tools/tts/field-reference#param-app-key)
- <a id="param-base-url-7" />[param-base-url-7](/tools/tts/field-reference#param-base-url-7)
- <a id="param-speaker-voice-5" />[param-speaker-voice-5](/tools/tts/field-reference#param-speaker-voice-5)
- <a id="param-speed-ratio" />[param-speed-ratio](/tools/tts/field-reference#param-speed-ratio)
- <a id="param-emotion" />[param-emotion](/tools/tts/field-reference#param-emotion)
- <a id="param-app-id-token-cluster" />[param-app-id-token-cluster](/tools/tts/field-reference#param-app-id-token-cluster)
- <a id="xai-1" />[xai-1](/tools/tts/field-reference#xai)
- <a id="param-api-key-9" />[param-api-key-9](/tools/tts/field-reference#param-api-key-9)
- <a id="param-base-url-8" />[param-base-url-8](/tools/tts/field-reference#param-base-url-8)
- <a id="param-speaker-voice-id-4" />[param-speaker-voice-id-4](/tools/tts/field-reference#param-speaker-voice-id-4)
- <a id="param-language" />[param-language](/tools/tts/field-reference#param-language)
- <a id="param-response-format-2" />[param-response-format-2](/tools/tts/field-reference#param-response-format-2)
- <a id="param-speed-2" />[param-speed-2](/tools/tts/field-reference#param-speed-2)
- <a id="xiaomi-mimo-1" />[xiaomi-mimo-1](/tools/tts/field-reference#xiaomi-mimo)
- <a id="param-api-key-10" />[param-api-key-10](/tools/tts/field-reference#param-api-key-10)
- <a id="param-base-url-9" />[param-base-url-9](/tools/tts/field-reference#param-base-url-9)
- <a id="param-model-5" />[param-model-5](/tools/tts/field-reference#param-model-5)
- <a id="param-speaker-voice-6" />[param-speaker-voice-6](/tools/tts/field-reference#param-speaker-voice-6)
- <a id="param-format" />[param-format](/tools/tts/field-reference#param-format)
- <a id="param-style" />[param-style](/tools/tts/field-reference#param-style)

## Service links

- [Azure Speech provider](/providers/azure-speech)
- [Azure Speech REST text-to-speech](https://learn.microsoft.com/azure/ai-services/speech-service/rest-text-to-speech)
- [ElevenLabs Authentication](https://elevenlabs.io/docs/api-reference/authentication)
- [ElevenLabs Text to Speech](https://elevenlabs.io/docs/api-reference/text-to-speech)
- [Gradium](/providers/gradium)
- [Inworld TTS API](https://docs.inworld.ai/tts/tts)
- [Microsoft Speech output formats](https://learn.microsoft.com/azure/ai-services/speech-service/rest-text-to-speech#audio-outputs)
- [MiniMax T2A v2 API](https://platform.minimaxi.com/document/T2A%20V2)
- [node-edge-tts](https://github.com/SchneeHertz/node-edge-tts)
- [OpenAI Audio API reference](https://platform.openai.com/docs/api-reference/audio)
- [OpenAI text-to-speech guide](https://platform.openai.com/docs/guides/text-to-speech)
- [speech-core](https://github.com/soniqo/speech-core)
- [Speech Swift](https://github.com/soniqo/speech-swift)
- [Volcengine TTS HTTP API](/providers/volcengine#text-to-speech)
- [xAI text to speech](https://docs.x.ai/developers/rest-api-reference/inference/voice#text-to-speech-rest)
- [Xiaomi MiMo speech synthesis](/providers/xiaomi#text-to-speech)

## Related

- [Media overview](/tools/media-overview)
- [Media playback](/nodes/media-playback)
- [Music generation](/tools/music-generation)
- [Video generation](/tools/video-generation)
- [Slash commands](/tools/slash-commands)
- [Voice call plugin](/plugins/voice-call)
