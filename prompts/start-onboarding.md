# Start Onboarding Prompt

Use this prompt in Codex, GitHub Copilot, Claude, Gemini, or another AI tool that can read repository files.

```text
Start onboarding for this repository.

Read README.md and AGENTS.md.
Then read .agents/skills/wp-onboarding/SKILL.md.

If project-context.md does not exist, create it through the onboarding workflow.
Keep onboarding short. Ask only the basic questions needed to create a useful first version of project-context.md.
Before asking questions, tell me that onboarding creates only a first version of project-context.md.
Also tell me that I can manually edit project-context.md at any time later, so I do not need to provide perfect or complete answers now.

Do not write an article yet.
Do not publish anything to WordPress.
```
