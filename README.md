# LLM From Scratch

A hands-on project following the course **"Build a Large Language Model (From Scratch)"** by Sebastian Raschka.

## Resources

- **YouTube Playlist:** [Build an LLM from Scratch](https://www.youtube.com/watch?v=yAcWnfsZhzo&list=PLTKMiZHVd_2IIEsoJrWACkIxLRdfMlw11)
- **GitHub Repository:** [rasbt/LLMs-from-scratch](https://github.com/rasbt/LLMs-from-scratch)
- **Book:** *Build a Large Language Model (From Scratch)* — Sebastian Raschka (Manning Publications)

## What This Course Covers

1. **Tokenization** — Converting raw text into tokens; BPE tokenizer
2. **Attention Mechanisms** — Self-attention, scaled dot-product attention, multi-head attention
3. **GPT Architecture** — Building a GPT-2-like transformer model from scratch using PyTorch
4. **Pretraining** — Training the model on raw text data
5. **Fine-tuning** — Instruction fine-tuning and classification fine-tuning
6. **Loading Pretrained Weights** — Loading OpenAI's GPT-2 weights into the custom model

## Setup

```bash
pip install uv
uv venv .venv
source .venv/Scripts/activate   # bash
# or
.venv\Scripts\Activate.ps1      # PowerShell

uv pip install -r requirements.txt
```

## Requirements

- Python 3.10+
- PyTorch
- tiktoken
- numpy
- matplotlib
- jupyter

## Add .gitignore

```bash
curl -o .gitignore https://raw.githubusercontent.com/github/gitignore/main/Python.gitignore
```