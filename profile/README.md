# RunAnywhere

Inference research at the frontier. Our agents build the kernels for each chip, and Wally ships the tokens.

RunAnywhere is a research-led inference company. You can use frontier open models through Wally's API and CLI today.

Sanchit Monga and Shubham Malhotra met at RIT in 2019 and started RunAnywhere in 2025 to run AI on the devices people already own. After YC W26 and the open-source SDKs, our AI agents built engines for Apple silicon and Hexagon NPUs. Wally launched in September 2026 because the models people wanted no longer fit on a phone or laptop. We open-sourced trnRT for AWS Trainium in October.

## Research

The trnRT results are self-run, one run per point, and are not official InferenceX results. There is no GPU baseline on the same traces yet. The GLM-5.3-Flash on Trainium2 post is by Aman Swar and Sanchit Monga; the trnRT launch post is by Aman Swar and Shubham Malhotra.

| Work | Hardware | Model and workload | Result and conditions | Authors | Read |
| --- | --- | --- | --- | --- | --- |
| [trnRT](https://github.com/RunanywhereAI/trnrt) | AWS Trainium2, one trn2.48xlarge | GLM-5.3-Flash; SemiAnalysis AgentX | Up to 3.57M tokens/min; ~95% cached input | Aman Swar and Sanchit Monga | [Method](https://runanywhere.ai/blog/glm-5-3-flash-trainium2-nki-megakernels) |
| [trnRT](https://github.com/RunanywhereAI/trnrt) | AWS Trainium2, half-box setup | GLM-5.3-Flash; 1,039,912-token prompt | 190.8 s to first token | Aman Swar and Sanchit Monga | [Method](https://runanywhere.ai/blog/glm-5-3-flash-trainium2-nki-megakernels) |
| MetalRT | Apple M4 Max, 64 GB | LLM decode, Qwen3-0.6B 4-bit | 658 tok/s, highest decode throughput across 5 runs; closed binary | Aman Swar and Shubham Malhotra | [Research](https://runanywhere.ai/research) |
| QHexRT | Hexagon NPU, v81 | LFM 2.5 230M; prefill | 12,540 tok/s on this model and chip configuration | Aman Swar and Shubham Malhotra | [Research](https://runanywhere.ai/research) |
| [RunAnywhere SDKs](https://github.com/RunanywhereAI/runanywhere-sdks) | On-device | Shared C++ core | SDKs for Swift, Kotlin, React Native, Flutter, TypeScript and C++ | | [Source](https://github.com/RunanywhereAI/runanywhere-sdks) |

## Use it

- **[Wally](https://runwally.com)** serves frontier open models through an OpenAI-compatible API and the `wally` CLI. Zero data retention by default. Works with OpenCode, Claude Code, Codex, Hermes and Cline.
- **[trnRT](https://github.com/RunanywhereAI/trnrt)** is an Apache-2.0 LLM inference engine for AWS Trainium. Start with the README.
- **[RunAnywhere SDKs](https://github.com/RunanywhereAI/runanywhere-sdks)** are open source. Use them to run models on-device in your app.

To set up Wally, tell your agent:

```text
set up https://runanywhere.ai/SKILL.md
```

## How we work

1. Start with a model, a chip and a workload.
2. Our AI agents build the kernels and the serving stack.
3. Publish the method and the limits alongside the result.

## Team

| Name | Work | GitHub |
| --- | --- | --- |
| Sanchit Monga | Co-founder and CEO; co-author of the GLM-5.3-Flash on Trainium2 post | [@sanchitmonga22](https://github.com/sanchitmonga22) |
| Shubham Malhotra | Co-founder and CTO; leads engine research; peer-reviewed researcher; co-author of the trnRT launch post with Aman Swar | [@shubhammalhotra28](https://github.com/shubhammalhotra28) |
| Aman Swar | Founding Engineer, ML systems; Trainium NKI kernels and speculative decoding | [@AmanSwar](https://github.com/AmanSwar) |
| Siddhesh Sonar | Engineer; on-device SDKs, the wally CLI and the website | [@Siddhesh2377](https://github.com/Siddhesh2377) |
| Aditya Batra | GTM and Developer Relations; open-model community and integrations | [@adityabatra072](https://github.com/adityabatra072) |

## Links

[RunAnywhere](https://runanywhere.ai) · [Research](https://runanywhere.ai/research) · [Wally](https://runwally.com) · [X @RunAnywhereAI](https://x.com/RunAnywhereAI)
