<p align="center">
  <img src="skills/ez/assets/ez-header.png" alt="Glossy red eZ push button" width="100%">
</p>

# ez

ez is a skills-only plugin for ChatGPT and Codex. Its bundled skill chooses a cost-appropriate model and reasoning level, explains the choice, and then completes the original request.

## Usage

Invoke the skill explicitly and include the task you want completed:

```text
$ez Fix the failing tests in this repository.
```

ez reports the selected model, reasoning level, rationale, and confidence before delegating the work.

## Local installation

Add this repository to a local plugin marketplace, install `ez` from the Plugins Directory, and restart the ChatGPT desktop app. For direct skill development, copy `skills/ez` into a supported skills directory.

## Public distribution

Create a ZIP whose root contains `plugin.json` and `skills/`, then upload it as a new plugin in the OpenAI Plugins dashboard. Resolve automated findings, submit it for review, and publish the approved version to make it discoverable in the shared ChatGPT and Codex plugin directory.

## Structure

- `plugin.json` - portable plugin identity and public listing metadata
- `skills/ez/SKILL.md` - routing behavior and execution instructions
- `skills/ez/agents/openai.yaml` - skill UI metadata and invocation policy
- `skills/ez/assets/` - header artwork and skill icons

The skill is configured for explicit invocation with `$ez`.
