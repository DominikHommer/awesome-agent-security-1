# Awesome Agent Security [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Securing autonomous AI agents — configs, runtime, tools, MCP, and red-teaming.

A curated list of resources for securing AI **agents** specifically: the skills, plugins, MCP servers, hooks, and unattended loops that execute with your credentials. General LLM-safety lists are linked at the bottom; this one is about the agent attack surface — static config risks, runtime behavior, tool/MCP poisoning, and prompt injection.

*Prompt injection is the SQL injection of the agent era — #1 on the OWASP LLM Top 10, because it exploits the trust boundary between untrusted input and a tool-wielding agent.*

## Contents

- [Threat Models & Standards](#threat-models--standards)
- [Static & Config Scanning](#static--config-scanning)
- [Runtime Guardrails](#runtime-guardrails)
- [Red-Teaming & Testing](#red-teaming--testing)
- [Prompt Injection & Tool Poisoning](#prompt-injection--tool-poisoning)
- [Related Lists](#related-lists)
- [Contributing](#contributing)

## Threat Models & Standards

- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/) - The canonical risk taxonomy; prompt injection sits at #1.
- [OWASP Top 10 for Agentic Applications (ASI)](https://www.promptfoo.dev/docs/red-team/owasp-agentic-ai/) - Agent-specific risks: goal hijack, tool misuse, identity/privilege abuse (Dec 2025 release, ASI prefix).

## Static & Config Scanning

- [agentvet](https://github.com/adventurewave-labs/agentvet) - Scans an agentic workspace (skills, plugins, subagents, hooks, MCP configs, CLAUDE.md) for injection, exfiltration, and over-permissioning before an agent runs. *(ours)*
- [mcp-scan](https://github.com/invariantlabs-ai/mcp-scan) - Invariant's scanner for MCP servers: inventories installed components and flags injections, sensitive-data handling, and hidden payloads.

## Runtime Guardrails

- [agent-warden](https://github.com/adventurewave-labs/agent-warden) - eBPF runtime guardrails: watches what agents actually do (files, egress, process spawns) and enforces alert/block/kill. *(ours)*
- [LLM Guard](https://github.com/protectai/llm-guard) - Protect AI's security toolkit for LLM I/O: sanitization, harmful-content detection, data-leak prevention, prompt-injection resistance.
- [NeMo Guardrails](https://github.com/NVIDIA-NeMo/Guardrails) - NVIDIA's toolkit for programmable rails between app code and the model.

## Red-Teaming & Testing

- [garak](https://github.com/NVIDIA/garak) - NVIDIA's LLM vulnerability scanner — nmap for language models; the widest range of attack probes.
- [PyRIT](https://github.com/microsoft/PyRIT) - Microsoft's Python Risk Identification Tool for proactively finding risks in generative-AI systems.
- [promptfoo](https://github.com/promptfoo/promptfoo) - Test/red-team harness with first-class CI/CD support and an agentic red-team suite (now an OpenAI product; still open source).

## Prompt Injection & Tool Poisoning

- [mcp-injection-experiments](https://github.com/invariantlabs-ai/mcp-injection-experiments) - Reproducible proof-of-concept MCP tool-poisoning attacks — read these before you trust a tool description.
- [Simon Willison — prompt injection](https://simonwillison.net/tags/prompt-injection/) - The running field notes on prompt injection: why it's unsolved and what actually helps.

## Related Lists

- [awesome-ai-security](https://github.com/ottosulin/awesome-ai-security) - Broad AI-security resource collection.
- [Awesome-LLMSecOps](https://github.com/wearetyomsmnv/Awesome-LLMSecOps) - LLM security operations: tooling, attacks, defenses.
- [awesome-agent-skills-security](https://github.com/LLMSecurity/awesome-agent-skills-security) - Focused on agent-skill security: attacks, defenses, benchmarks for tool use.

## Contributing

PRs welcome — one entry per PR, with a one-line reason it belongs here. Must be agent-security specific (not generic infosec or generic ML). No dead links, no vendor pages without substance. See [CONTRIBUTING.md](CONTRIBUTING.md).

---

Maintained by [Adventure Wave Labs](https://github.com/adventurewave-labs) — we also build [agentvet](https://github.com/adventurewave-labs/agentvet) and [agent-warden](https://github.com/adventurewave-labs/agent-warden).

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](LICENSE)
