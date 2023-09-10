---
library_name: peft
license: apache-2.0
tags:
- llama2
- quantization
- nlp
- transformers
- language-model
- bitsandbytes
- fine-tuned
- causal-lm
datasets:
- timdettmers/openassistant-guanaco
---

## Overview

This model is a fine-tuned model based on the "TinyPixel/Llama-2-7B-bf16-sharded" model and "timdettmers/openassistant-guanaco" dataset. It is optimized for causal language modeling tasks with specific quantization configurations. The model is trained using the PEFT framework and leverages the `bitsandbytes` quantization method.

## Training Procedure

The following `bitsandbytes` quantization config was used during training:

- quant_method: bitsandbytes
- load_in_8bit: False
- load_in_4bit: True
- llm_int8_threshold: 6.0
- llm_int8_skip_modules: None
- llm_int8_enable_fp32_cpu_offload: False
- llm_int8_has_fp16_weight: False
- bnb_4bit_quant_type: nf4
- bnb_4bit_use_double_quant: False
- bnb_4bit_compute_dtype: float16

### Framework Versions

The model was trained using PEFT version 0.6.0.dev0.