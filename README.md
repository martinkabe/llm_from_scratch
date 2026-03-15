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

## Create and initialize new repository

```bash
cd ~/Projects/LLMs/llm_from_scratch

git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/martinkabe/llm_from_scratch.git
git push -u origin main
```

**Fix — clear the old cached credentials and re-authenticate:**

```bash
git credential reject <<EOF
protocol=https
host=github.com
EOF

git push -u origin main
```

If that doesn't work, use a Personal Access Token (PAT) explicitly in the remote URL:

1. Generate a PAT at: GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic) — give it repo scope.
2. Update the remote:

```bash
git remote set-url origin https://martinkabe@github.com/martinkabe/llm_from_scratch.git
```



## Troubleshooting SSL certificate errors

* Some readers reported seeing ssl.SSLCertVerificationError: `SSL: CERTIFICATE_VERIFY_FAILED` when running `urllib.request.urlretrieve` in VSCode or Jupyter.
* This usually means Python's certificate bundle is outdated.

**Fixes**

* Use Python ≥ 3.9; you can check your Python version by executing the following code:

```
importsys
print(sys.__version__)
```

* Upgrade the cert bundle:
  * pip: `pip install --upgrade certifi`
  * uv: `uv pip install --upgrade certifi`
* Restart the Jupyter kernel after upgrading.
* If you still encounter an `ssl.SSLCertVerificationError` when executing the previous code cell, please see the discussion at [more information here on GitHub](https://github.com/rasbt/LLMs-from-scratch/pull/403)
