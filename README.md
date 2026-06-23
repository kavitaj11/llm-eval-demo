# LLM Eval Demo Target

This repository is a **demo target** for the [LLM Eval Agent](https://github.com/K11-Software-Solutions/llm-eval-agent-app) GitHub App.

When a pull request is opened that changes a model config, prompt file, or data file,
the LLM Eval Agent automatically runs bias, fairness, and robustness checks and posts
the results directly on the PR as a GitHub Check Run.

## How it works

1. Open a PR that changes any file in `config/`, `prompts/`, or `data/`
2. The LLM Eval Agent webhook fires
3. Bias, fairness, and robustness evaluation runs automatically
4. Results are posted as a GitHub Check on the PR

## Repository structure

```
config/
  model_config.yaml       <- model under evaluation (changing this triggers eval)
prompts/
  system_prompt.txt       <- prompt template (changing this triggers eval)
data/
  sample_eval_data.jsonl  <- evaluation dataset
```

## Try it

1. Fork this repo or clone it
2. Create a branch: `git checkout -b update-model-v2`
3. Edit `config/model_config.yaml` — change the model name
4. Open a PR
5. Watch the LLM Eval Agent post results on your PR

## About LLM Eval Agent

The LLM Eval Agent is a shift-left LLM safety tool — it catches bias and fairness issues
before they reach production, embedded directly in the GitHub pull request workflow.

Built with: FastAPI · LangTest · HuggingFace Transformers · GitHub Apps API

Copyright 2026 Kavita Jadhav / K11 Software Solutions LLC — Apache 2.0 License
