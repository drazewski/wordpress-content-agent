# Start Onboarding Prompt

Use this prompt in Codex, GitHub Copilot, Claude, Gemini, or another AI tool that can read repository files.

```text
Start onboarding for this repository.

Read README.md and AGENTS.md.
Then read .agents/skills/onboarding/SKILL.md.

If project-context.md does not exist, create it through the onboarding workflow.
Keep onboarding short. Ask only the basic questions needed to create a useful first version of project-context.md.
Ask exactly one onboarding question at a time and wait for my answer before asking the next one.
Ask whether I want the optional WordPress draft step after the local Markdown file is created.
Treat local Markdown export to articles/ as always enabled.
Before asking questions, tell me that onboarding creates only a first version of project-context.md.
Also tell me that I can manually edit project-context.md at any time later, so I do not need to provide perfect or complete answers now.

Do not write an article yet.
Do not publish anything.
```
