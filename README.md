# Awesome Agent Security [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Securing autonomous AI agents — configs, runtime, tools, MCP, and red-teaming.

A curated list of resources for securing AI **agents** specifically: the skills, plugins, MCP servers, hooks, and unattended loops that execute with your credentials. General LLM-safety lists are linked at the bottom; this one is about the agent attack surface — static config risks, runtime behavior, tool/MCP poisoning, and prompt injection.

*Prompt injection is the SQL injection of the agent era — #1 on the OWASP LLM Top 10, because it exploits the trust boundary between untrusted input and a tool-wielding agent.*

## Contents

- [Threat Models & Standards](#threat-models--standards)
- [Static & Config Scanning](#static--config-scanning)
- [Runtime Guardrails](#runtime-guardrails)
- [Red-Teaming & Testing](#red-teaming--testing)
- [Benchmarks & Evaluation](#benchmarks--evaluation)
- [Prompt Injection & Tool Poisoning](#prompt-injection--tool-poisoning)
- [Identity, Authorization & Access](#identity-authorization--access)
- [Related Lists](#related-lists)
- [Contributing](#contributing)

## Threat Models & Standards

- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/) - The canonical risk taxonomy; prompt injection sits at #1.
- [OWASP Top 10 for Agentic Applications (ASI)](https://www.promptfoo.dev/docs/red-team/owasp-agentic-ai/) - Agent-specific risks: goal hijack, tool misuse, identity/privilege abuse (Dec 2025 release, ASI prefix).

## Static & Config Scanning

- [agent-scan](https://github.com/snyk/agent-scan) - Scanner for MCP servers and AI agents: inventories installed components and flags injections, sensitive-data handling, and hidden payloads. Formerly Invariant Labs' mcp-scan; now maintained by Snyk.

## Runtime Guardrails

- [LLM Guard](https://github.com/protectai/llm-guard) - Protect AI's security toolkit for LLM I/O: sanitization, harmful-content detection, data-leak prevention, prompt-injection resistance. Archived by its maintainer as of Jul 2026; no linked successor.
- [NeMo Guardrails](https://github.com/NVIDIA-NeMo/Guardrails) - NVIDIA's toolkit for programmable rails between app code and the model.
- [Guardrails AI](https://github.com/guardrails-ai/guardrails) - Input/output Guards backed by a Hub of composable validators; structured-output enforcement plus risk detection.

## Red-Teaming & Testing

- [garak](https://github.com/NVIDIA/garak) - NVIDIA's LLM vulnerability scanner — nmap for language models; the widest range of attack probes.
- [PyRIT](https://github.com/microsoft/PyRIT) - Microsoft's Python Risk Identification Tool for proactively finding risks in generative-AI systems.
- [promptfoo](https://github.com/promptfoo/promptfoo) - Test/red-team harness with first-class CI/CD support and an agentic red-team suite (now an OpenAI product; still open source).

## Benchmarks & Evaluation

- [AgentDojo](https://github.com/ethz-spylab/agentdojo) - ETH Zurich's dynamic environment for evaluating prompt-injection attacks and defenses on tool-using agents across banking, Slack, workspace, and travel tasks.
- [InjecAgent](https://github.com/uiuc-kang-lab/InjecAgent) - Benchmark for indirect prompt injection in tool-integrated agents: 1,054 cases spanning 17 user tools and 62 attacker tools.

## Prompt Injection & Tool Poisoning

- [mcp-injection-experiments](https://github.com/invariantlabs-ai/mcp-injection-experiments) - Reproducible proof-of-concept MCP tool-poisoning attacks — read these before you trust a tool description.
- [vigil-llm](https://github.com/deadbits/vigil-llm) - Self-hostable scanner (library + REST API) that detects prompt injections and jailbreaks, shipping its own signatures and datasets. Last released Dec 2023; largely unmaintained since.
- [Simon Willison — prompt injection](https://simonwillison.net/tags/prompt-injection/) - The running field notes on prompt injection: why it's unsolved and what actually helps.

## Identity, Authorization & Access

- [Cerbos](https://github.com/cerbos/cerbos) - Policy-as-code, language-agnostic authorization; enforce fine-grained, context-aware access control on which tools an agent may call (ships an MCP authorization demo).

## Related Lists

- [awesome-ai-security](https://github.com/ottosulin/awesome-ai-security) - Broad AI-security resource collection.
- [Awesome-LLMSecOps](https://github.com/wearetyomsmnv/Awesome-LLMSecOps) - LLM security operations: tooling, attacks, defenses.
- [awesome-agent-skills-security](https://github.com/LLMSecurity/awesome-agent-skills-security) - Focused on agent-skill security: attacks, defenses, benchmarks for tool use.

## Contributing

PRs welcome — one entry per PR, with a one-line reason it belongs here. Must be agent-security specific (not generic infosec or generic ML). No dead links, no vendor pages without substance. See [CONTRIBUTING.md](CONTRIBUTING.md).

---

Maintained by [Adventure Wave Labs](https://github.com/adventurewave-labs).

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](LICENSE)
