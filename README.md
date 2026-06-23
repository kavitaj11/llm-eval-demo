# llm-eval-demo

Demo repository for the [LLM Eval Agent](https://github.com/K11-Software-Solutions/llm-eval-agent-app) GitHub App.

## What this repo demonstrates

Every pull request that changes `config/model_config.yaml` or prompt files automatically triggers a bias and fairness evaluation via the LLM Eval Agent GitHub App.

## How it works

1. Open a PR modifying `config/model_config.yaml`
2. The LLM Eval Agent webhook fires automatically
3. A Check Run appears on the PR with live eval status
4. Results are posted as a PR comment scorecard

## Configuration

See `config/model_config.yaml` for the model and evaluation thresholds used in this demo.
