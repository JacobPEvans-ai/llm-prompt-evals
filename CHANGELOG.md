# Changelog

## [0.8.1](https://github.com/JacobPEvans-ai/llm-prompt-evals/compare/v0.8.0...v0.8.1) (2026-11-12)


### Bug Fixes

* replace private names with role words ([#189](https://github.com/JacobPEvans-ai/llm-prompt-evals/issues/189)) ([a7d7cf6](https://github.com/JacobPEvans-ai/llm-prompt-evals/commit/a7d7cf69c91edd7352c2cc1cc2d8e5b17e08a448))

## [0.8.0](https://github.com/dryvist/llm-prompt-evals/compare/v0.7.0...v0.8.0) (2026-11-09)


### Features

* **agent:** opencode-local run j-3c547b78f4801bc1 ([bf1a245](https://github.com/dryvist/llm-prompt-evals/commit/bf1a24562555e742342169307053eacdcfdf8488))
* **agent:** opencode-local run j-5e04b33111213103 ([3a1b977](https://github.com/dryvist/llm-prompt-evals/commit/3a1b97766942153d0c34a90371da9adaf7261b10))
* **evals:** read the benchmark router key through OpenBao and run all fabric suites ([#184](https://github.com/dryvist/llm-prompt-evals/issues/184)) ([dccdf43](https://github.com/dryvist/llm-prompt-evals/commit/dccdf43c322fb7c6d4a93b494a29ee163a54fd0c))


### Bug Fixes

* **evals:** run the agentic and tool-queries suites on the local fabric ([#181](https://github.com/dryvist/llm-prompt-evals/issues/181)) ([bf1a245](https://github.com/dryvist/llm-prompt-evals/commit/bf1a24562555e742342169307053eacdcfdf8488))
* **evals:** run the agentic-mcp suite on the local fabric ([#182](https://github.com/dryvist/llm-prompt-evals/issues/182)) ([3a1b977](https://github.com/dryvist/llm-prompt-evals/commit/3a1b97766942153d0c34a90371da9adaf7261b10))

## [0.7.0](https://github.com/dryvist/llm-prompt-evals/compare/v0.6.0...v0.7.0) (2026-11-09)


### Features

* **agent:** opencode-local run j-f7cbc48399294f21 ([3d7b49b](https://github.com/dryvist/llm-prompt-evals/commit/3d7b49bd6aa5458382aaa0446466b431b793a41d))


### Bug Fixes

* **ci:** set up Node before promptfoo on the self-hosted runners ([#175](https://github.com/dryvist/llm-prompt-evals/issues/175)) ([8e42b16](https://github.com/dryvist/llm-prompt-evals/commit/8e42b16ba3faa2e61aa97e12bb2b5605fc418d01))
* **fabric:** make the triage and spl suite configs validate under promptfoo 0.124.1 ([#178](https://github.com/dryvist/llm-prompt-evals/issues/178)) ([3d7b49b](https://github.com/dryvist/llm-prompt-evals/commit/3d7b49bd6aa5458382aaa0446466b431b793a41d))

## [0.6.0](https://github.com/dryvist/llm-prompt-evals/compare/v0.5.1...v0.6.0) (2026-11-09)


### Features

* **eval:** schedule a local benchmark matrix every six hours ([#172](https://github.com/dryvist/llm-prompt-evals/issues/172)) ([d2da109](https://github.com/dryvist/llm-prompt-evals/commit/d2da109fdd89f3cf2a026532e666cabb4ecd9009))

## [0.5.1](https://github.com/dryvist/llm-prompt-evals/compare/v0.5.0...v0.5.1) (2026-11-05)


### Bug Fixes

* **evals:** grade the fabric eval on the local router ([#151](https://github.com/dryvist/llm-prompt-evals/issues/151)) ([c1efe64](https://github.com/dryvist/llm-prompt-evals/commit/c1efe6490a32d4f49d9fa3b97afafbb74172874a))

## [0.5.0](https://github.com/dryvist/llm-prompt-evals/compare/v0.4.0...v0.5.0) (2026-11-03)


### Features

* **evals:** route the held-out suite through the org router ([#144](https://github.com/dryvist/llm-prompt-evals/issues/144)) ([83244a2](https://github.com/dryvist/llm-prompt-evals/commit/83244a28fe0698147b8399858a56e19e0b1b4227))

## [0.4.0](https://github.com/dryvist/llm-prompt-evals/compare/v0.3.0...v0.4.0) (2026-10-26)


### Features

* **evals:** gate a candidate prompt on the held-out Langfuse dataset against its baseline ([#141](https://github.com/dryvist/llm-prompt-evals/issues/141)) ([d57f01a](https://github.com/dryvist/llm-prompt-evals/commit/d57f01a93c7aeaf261f5a3e9b7208abb6b0b25f2))

## [0.3.0](https://github.com/dryvist/llm-prompt-evals/compare/v0.2.0...v0.3.0) (2026-10-23)


### Features

* add pinned public repository QA suite ([#125](https://github.com/dryvist/llm-prompt-evals/issues/125)) ([6cddbb5](https://github.com/dryvist/llm-prompt-evals/commit/6cddbb52c4bda678eef3b44c4df90e5798d33218))
* add pinned public-repository QA suite ([2e1976f](https://github.com/dryvist/llm-prompt-evals/commit/2e1976fb44b689fa97802cf34b3e930a8c14119f))
* **repo-qa:** give the xhigh arm the full output budget ([3d7893c](https://github.com/dryvist/llm-prompt-evals/commit/3d7893caba43013f6bdd7671d29f3a42a6b0e515))
* **repo-qa:** match answers case-insensitively and add xhigh arm ([7999b7c](https://github.com/dryvist/llm-prompt-evals/commit/7999b7cbe7f228b4b23023f1087d7b822c26c545))
* **repo-qa:** raise the reasoning-off output cap ([bfc093d](https://github.com/dryvist/llm-prompt-evals/commit/bfc093d98499adbb8f54120e059f45109f7fedfe))


### Bug Fixes

* **agentic:** reword the suite description and prompt history wording ([#130](https://github.com/dryvist/llm-prompt-evals/issues/130)) ([3488d6e](https://github.com/dryvist/llm-prompt-evals/commit/3488d6ebe4bf9bf4b0663f3fc8a5e5b309d7cf7a))
* configure homelab access OFF arm ([665d0dc](https://github.com/dryvist/llm-prompt-evals/commit/665d0dcf040b9be8cea0a5526649daa133566696))
* **devshell:** use the system git instead of a pinned git ([80feff1](https://github.com/dryvist/llm-prompt-evals/commit/80feff199b077c779a394554833bb26f90b84e0d))
* **homelab-access:** parse provider output only when it is JSON ([b710129](https://github.com/dryvist/llm-prompt-evals/commit/b7101295b4dd94510ec0f2ecb538804c0b9e35c4))
* **homelab-access:** stop requiring a tool call on ask and refuse cases ([9ccbdcc](https://github.com/dryvist/llm-prompt-evals/commit/9ccbdcce5ce888827d9ff2593be0dd1163526c55))
* restore release metadata baseline ([#134](https://github.com/dryvist/llm-prompt-evals/issues/134)) ([e89e1a1](https://github.com/dryvist/llm-prompt-evals/commit/e89e1a1e7639164ff653af7cba18445334ec0358))

## [0.2.0](https://github.com/dryvist/llm-prompt-evals/compare/v0.1.0...v0.2.0) (2026-10-16)


### Features

* add domain eval suites ([8ae6ca2](https://github.com/dryvist/llm-prompt-evals/commit/8ae6ca20289d7f771328a5ad7e1996b63a0fb7e6))
* add domain eval suites ([#116](https://github.com/dryvist/llm-prompt-evals/issues/116)) ([139a92f](https://github.com/dryvist/llm-prompt-evals/commit/139a92f0de1d13ca9e47a69a2f9c1de29d61bd0e))
* use native Promptfoo assertions for domain suites ([d68c303](https://github.com/dryvist/llm-prompt-evals/commit/d68c3035ab6a6449a3c75b8663e85f7d7e363fd4))

## 0.1.0 (2026-07-20)


### Features

* **demo:** end-to-end log-monitoring prompt-eval demo ([#6](https://github.com/dryvist/llm-prompt-evals/issues/6)) ([76899db](https://github.com/dryvist/llm-prompt-evals/commit/76899db2cf85ffff3494082d96c9d8636e9d24f4))
* scaffold promptfoo prompt-eval framework ([#1](https://github.com/dryvist/llm-prompt-evals/issues/1)) ([65974c0](https://github.com/dryvist/llm-prompt-evals/commit/65974c01e4f219e029432531fdd1518aee744bdb))


### Miscellaneous

* **release:** promote develop to main ([556779a](https://github.com/dryvist/llm-prompt-evals/commit/556779a479cb50163869240dfc4ad2124bc8408f))
