# GPT-2 small / Goldilocks workspace

This is the initial workspace for a Rust implementation of standard GPT-2 small quantized inference. It contains reference inputs and environment information only; no inference implementation is provided.

## Inputs

- references/zkGPT-USENIXSecurity2025.pdf: official zkGPT paper.
- references/zkGPT-source.json: paper source and checksum.
- references/gpt2-config.json: standard GPT-2 small configuration.
- references/gpt2-source.json: exact model revision, published weight checksum, and local weight path.
- assets/gpt2/model.safetensors: pre-downloaded full model weights; intentionally excluded from Git because of size.
- assets/gpt2/config.json: model configuration beside the weights.

For a fresh clone, download model.safetensors from the pinned Hugging Face model revision in references/gpt2-source.json and verify its SHA256 before use. The source URL pattern is https://huggingface.co/{model_id}/resolve/{revision}/model.safetensors .

## Environment

Linux CPU environment. Plonky3 p3-goldilocks and p3-field version 0.7.0 were compiled successfully with rustc/cargo 1.97.1 using the installed stable toolchain. The task process is started with RUSTUP_TOOLCHAIN=stable; the user's global default is unchanged. Record an exact dependency lockfile as the new project is implemented.

The task process also receives a separate Python environment for optional floating-point reference libraries; no reference inference script is supplied. Run python through the inherited PATH. Compiler output is directed outside this repository by CARGO_TARGET_DIR.
