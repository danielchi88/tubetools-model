# Tube Tools AI model

The on-device AI model used by [Tube Tools by DC](https://github.com/danielchi88/tubetools) for transcript summaries and live chat reports. Tube Tools downloads these files the first time AI summaries are turned on, and runs them on the Mac with Apple's MLX; nothing is sent anywhere.

## Model

**Qwen 3.5 2B** by Alibaba Cloud ([Qwen/Qwen3.5-2B](https://huggingface.co/Qwen/Qwen3.5-2B)), unmodified apart from conversion to a text-only MLX model with 4-bit weights (group size 64):

```
mlx_lm.convert --hf-path Qwen/Qwen3.5-2B -q --q-bits 4 --q-group-size 64   # mlx-lm 0.32.2
```

## Files (release `qwen3.5-2b-4bit-v1`)

| File | Bytes | SHA-256 |
|---|---:|---|
| config.json | 2625 | `8893a91e9b7763d7b94c6db181f5b7c79c6f4881a69cefb11549eefcab1823bf` |
| model.safetensors | 1059404951 | `44610b29c3ce91189a28195a3ef4fc34634330a781b6faed61bcd4bf40855e39` |
| model.safetensors.index.json | 60786 | `3b2dffa510d1d73decdbc12d5e1bc7d6a9f7b2deb631bfd84238a1f8fc4e0fd1` |
| tokenizer.json | 19989339 | `a5cd9732badce41de57e6efce8302930ded1c1188c5f81feb2bd6c24c4a1941f` |
| tokenizer_config.json | 1502 | `4d2fc7899270dc76b57a7aa1d5ec3234e6a25934c6e2aea6166f989f1d453892` |
| chat_template.jinja | 7755 | `273d8e0e683b885071fb17e08d71e5f2a5ddfb5309756181681de4f5a1822d80` |

## License

Qwen 3.5 is licensed under the Apache License 2.0; see [LICENSE](LICENSE). This repository redistributes a converted copy under the same license. Copyright 2026 Alibaba Cloud.
