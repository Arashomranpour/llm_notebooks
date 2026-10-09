<div align="center">

# 📓 LLM Notebooks - Smart Model Router

**A Colab notebook showing how to route queries to different LLMs with LiteLLM, add fallbacks and guard against prompt injection.**

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![LiteLLM](https://img.shields.io/badge/LiteLLM-router-6A5ACD)
![Groq](https://img.shields.io/badge/Groq-F55036)
![Colab](https://img.shields.io/badge/Open_in-Colab-F9AB00?logo=googlecolab&logoColor=white)

</div>

---

## ✨ What's inside

`Untitled22.ipynb` builds a small "smart chat" pipeline on top of Groq-hosted models:

| Step | Description |
|---|---|
| 🏷️ **Task classification** | A short LLM call labels each query as `code`, `summary` or `general` |
| 🧭 **Routing** | Each task type maps to its own list of models |
| 🔁 **Fallback chain** | If a model fails, the next one in the list is tried automatically |
| 🛡️ **Guardrail** | A keyword-based check blocks obvious prompt-injection attempts before any model is called |

`smart_chat()` returns the detected task, the model that answered and the answer itself.

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Arashomranpour/llm_notebooks/blob/main/Untitled22.ipynb)

## 🚀 Getting Started

1. Create a [Groq API key](https://console.groq.com/keys).
2. Open the notebook in Colab and save the key as a Colab secret named `GROQ_API_KEY`.
3. Run all cells.

Locally:

```bash
git clone https://github.com/Arashomranpour/llm_notebooks.git
cd llm_notebooks
pip install litellm langchain langchain-groq
export GROQ_API_KEY=your_key
jupyter notebook Untitled22.ipynb
```

## 📁 Project Structure

```
.
├── Untitled22.ipynb
└── LICENSE
```

## 🛠️ Tech Stack

`LiteLLM` · `Groq` · `LangChain`
