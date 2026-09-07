# GPT-2 Goldilocks

A Rust project for deterministic quantized inference of GPT-2 small over the Goldilocks field.

## Reference materials

- `references/zkGPT-USENIXSecurity2025.pdf`: the zkGPT paper.
- `references/zkGPT-source.json`: publication details and PDF checksum.
- `references/gpt2-source.json`: pinned model revision, weight location, and checksums.
- `references/gpt2-config.json`: the standard GPT-2 configuration.
- `assets/gpt2/model.safetensors`: the full pretrained weights.
- `assets/gpt2/config.json`: the matching configuration.

The large weight file is excluded from Git. To obtain it again, use the pinned revision and SHA256 in `references/gpt2-source.json`.

## Development environment

Linux CPU, Rust 1.97.1 stable. Plonky3 `p3-goldilocks` and `p3-field` 0.7.0 are available. Python includes PyTorch CPU, Transformers, NumPy, and Safetensors for model conversion and floating-point reference calculations.
