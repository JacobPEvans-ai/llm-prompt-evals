# Demo: logmon prompt suite

One log-monitoring ("Hermes") base prompt rewritten by many AI models, every
rewrite scored on the same tests across several runner models. The published
report is `results/README.md`. Three configs share the prompt loader:

- `promptfooconfig.yaml` — base tier, `tests.yaml` (15 cases), all five
  runners.
- `promptfooconfig.hard.yaml` — hard tier, `tests-hard.yaml` (8 cases), all
  five runners.
- `promptfooconfig.fable.yaml` — premium-runner pass, `tests.yaml` on a
  curated 6-prompt subset, `fable-5-SUT` only.

Runner labels (`--filter-providers` accepts a label or a provider id):

- OpenRouter frontier: `opus-4.8-SUT`, `gemini-3-flash-SUT`,
  `deepseek-flash-SUT`.
- Org router (OpenAI-compatible): `qwen4-max-preview-SUT`
  (`openai:chat:qwen4-max-preview`), `qwen3.8-max-SUT`
  (`openai:chat:qwen3.8-max`).

## Credentials

All from the environment; the names are in `.env.example`. Never commit values.

- `OPENROUTER_API_KEY`: the OpenRouter runners and the default
  `claude-haiku-4.5` llm-rubric grader.
- `LLM_ROUTER_BASE_URL`: the org router's OpenAI-compatible base URL, ending
  in `/v1`. Unset runs fail against the `llm-router-unset.invalid` placeholder.
- `LLM_ROUTER_API_KEY`: the scoped router key the Qwen runners authenticate
  with.

## Run one model

Base and hard tiers, one runner per command (example: `qwen4-max-preview`):

```bash
promptfoo eval -c evals/demo-logmon/promptfooconfig.yaml \
  --filter-providers qwen4-max-preview-SUT \
  --output output/qwen4-max-preview-base.json

promptfoo eval -c evals/demo-logmon/promptfooconfig.hard.yaml \
  --filter-providers qwen4-max-preview-SUT \
  --output output/qwen4-max-preview-hard.json
```

For `qwen3.8-max`, use `--filter-providers qwen3.8-max-SUT` and the
`output/qwen3.8-max-*.json` names. Omit `--filter-providers` to run all five
runners in one pass.

## Where results land

- `--output` above writes each run's JSON under `output/` (gitignored).
- `./scripts/report.sh evals/demo-logmon/promptfooconfig.yaml` is the
  end-to-end flow for one config: it writes `output/latest.{json,html,md}`,
  `output/prompt_quality.json`, and `output/cost.json`, copies the HTML to
  `results/report.html`, and reassembles `results/README.md`.
- The published report combines tiers via the assembler:

```bash
node scripts/build_results.mjs \
  --main output/latest.json --hard output/hard.json \
  --quality output/prompt_quality.json --cost output/cost.json \
  --out results/README.md
```

The pass-count tables and the cost table (metered $ and subscription as
separate columns) enumerate providers from the run JSONs, so the Qwen columns
appear without further edits. The org-router aliases have no OpenRouter price,
so the cost report lists them at $0 metered; their traffic bills to the org
router account, not OpenRouter.

Commit `results/README.md` to publish on GitHub.
