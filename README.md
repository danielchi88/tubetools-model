# Tube Tools AI models

The on-device AI models used by [Tube Tools](https://github.com/danielchi88/tubetools) for transcript summaries and live chat reports. Tube Tools downloads a model when it's chosen in Settings ▸ AI, and runs it on the Mac with Apple's MLX; nothing is sent anywhere.

Each model is **Qwen 3.5** by Alibaba Cloud, unmodified apart from conversion to a text-only MLX model with 4-bit weights (group size 64), and splitting into files under 2 GB:

```
mlx_lm.convert --hf-path Qwen/Qwen3.5-<size> -q --q-bits 4 --q-group-size 64   # mlx-lm 0.32.2
```

## Release `qwen3.5-2b-4bit-v1` ([Qwen/Qwen3.5-2B](https://huggingface.co/Qwen/Qwen3.5-2B))

| File | Bytes | SHA-256 |
|---|---:|---|
| config.json | 2625 | `8893a91e9b7763d7b94c6db181f5b7c79c6f4881a69cefb11549eefcab1823bf` |
| model.safetensors.index.json | 60786 | `3b2dffa510d1d73decdbc12d5e1bc7d6a9f7b2deb631bfd84238a1f8fc4e0fd1` |
| tokenizer.json | 19989339 | `a5cd9732badce41de57e6efce8302930ded1c1188c5f81feb2bd6c24c4a1941f` |
| tokenizer_config.json | 1502 | `4d2fc7899270dc76b57a7aa1d5ec3234e6a25934c6e2aea6166f989f1d453892` |
| chat_template.jinja | 7755 | `273d8e0e683b885071fb17e08d71e5f2a5ddfb5309756181681de4f5a1822d80` |
| model.safetensors | 1059404951 | `44610b29c3ce91189a28195a3ef4fc34634330a781b6faed61bcd4bf40855e39` |

## Release `qwen3.5-4b-4bit-v1` ([Qwen/Qwen3.5-4B](https://huggingface.co/Qwen/Qwen3.5-4B))

| File | Bytes | SHA-256 |
|---|---:|---|
| config.json | 2878 | `8591d683d8d132234766399897415b9427967c05e77c1c169a40de3e81177e62` |
| model.safetensors.index.json | 91156 | `bb7b843792475e8854491daae7cc8e7172144666f44f23627af51002dd4c4a29` |
| tokenizer.json | 19989339 | `a5cd9732badce41de57e6efce8302930ded1c1188c5f81feb2bd6c24c4a1941f` |
| tokenizer_config.json | 1502 | `4d2fc7899270dc76b57a7aa1d5ec3234e6a25934c6e2aea6166f989f1d453892` |
| chat_template.jinja | 7756 | `a4aee8afcf2e0711942cf848899be66016f8d14a889ff9ede07bca099c28f715` |
| model-00001-of-00002.safetensors | 1890053900 | `5b04d1d7307994b7f33dccdf6212442f8d9b618fc6c263852380243de019e932` |
| model-00002-of-00002.safetensors | 477184216 | `6f14b6e47ccec840c4150dd5af340543e56a8c634560f32c09f6f2a1341f45ca` |

## Release `qwen3.5-9b-4bit-v1` ([Qwen/Qwen3.5-9B](https://huggingface.co/Qwen/Qwen3.5-9B))

| File | Bytes | SHA-256 |
|---|---:|---|
| config.json | 2843 | `15303ca367065b31713bb4573030718cdf1fc31d5bca5b4a989a68ef20e9540d` |
| model.safetensors.index.json | 91375 | `00af1791c841bd5b9351e0a8f9a777f937da1f68b1dff43244d23d53055011de` |
| tokenizer.json | 19989339 | `a5cd9732badce41de57e6efce8302930ded1c1188c5f81feb2bd6c24c4a1941f` |
| tokenizer_config.json | 1502 | `4d2fc7899270dc76b57a7aa1d5ec3234e6a25934c6e2aea6166f989f1d453892` |
| chat_template.jinja | 7756 | `a4aee8afcf2e0711942cf848899be66016f8d14a889ff9ede07bca099c28f715` |
| model-00001-of-00003.safetensors | 1896976352 | `b02284fcab1e2b05408ad4c378d4b69623da96bf362acc818076b532c6f656b2` |
| model-00002-of-00003.safetensors | 1900053728 | `b93f0787a06c943402d4c54faa3dc91a4bce2cb9d4ca099dde55497309a665e2` |
| model-00003-of-00003.safetensors | 1241131409 | `ac4a53009bed3ff647a621cf2e53f32cd51f03ac4c69e42bc3e5ccfded854d33` |

## License

Qwen 3.5 is licensed under the Apache License 2.0; see [LICENSE](LICENSE). This repository redistributes converted copies under the same license. Copyright 2026 Alibaba Cloud.
