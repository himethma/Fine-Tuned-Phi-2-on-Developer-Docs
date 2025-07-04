# Fine-Tuned-Phi-2-on-Developer-Docs
Fine-tuned Phi-2 model for generating Python documentation, REST API templates, and developer-style code snippets using the Lamini Docs dataset.
This repository contains a fine-tuned version of the [`microsoft/phi-2`](https://huggingface.co/microsoft/phi-2) language model, trained on the [`kotzeje/lamini_docs.json`](https://huggingface.co/datasets/kotzeje/lamini_docs) dataset to improve performance on generating realistic and practical Python documentation and code templates.


##  Overview
The base model (`phi-2`) was fine-tuned using supervised instruction tuning to enhance its ability to generate developer-style documentation, API templates, and code snippets. The fine-tuned model performs better than the base model on tasks such as:

- Generating Python docstrings
- Creating REST API templates using Flask
- Providing code examples aligned with developer documentation

##  Model Details

- **Base Model:** `microsoft/phi-2`
- **Dataset:** `kotzeje/lamini_docs.json`
- **Objective:** Instruction-tuned to improve performance on technical documentation and code generation tasks
- **Fine-Tuning Method:** Supervised learning with formatted instruction-response pairs

## Training Details

- **Fine-tuning Method:** LoRA (Low-Rank Adaptation)
- **Optimizer:** AdamW
- **Precision:** FP16
- **Training Configuration:**
  - Learning Rate: `3e-4`
  - Epochs: `3`
  - Batch Size: `4`
  - LoRA Rank: `8`
  - LoRA Alpha: `16`
  - Target Modules: `q_proj`, `v_proj`
  - Gradient Accumulation: `4`
  - Max Sequence Length: `2048`
 
## Intended Uses
This model is optimized for:
Generating Python docstrings
Creating REST API and Flask templates
Building developer documentation
Rapid prototyping for code examples
Instruction-based code generation

## Resources
Base Model: microsoft/phi-2 <br>
Training Dataset: kotzeje/lamini_docs <br>
🤗 https://huggingface.co/Himethma/phi-2-lamini-docs

## 📄 License

This project is licensed under the **MIT License**.




