<p align="center">
  <img src="assets/ez-header.png" alt="Glossy red eZ push button" width="100%">
</p>

# ez

ez is a Codex skill that chooses a cost-appropriate model and reasoning level, explains the choice, and then completes the original request.

## Usage

Invoke the skill explicitly and include the task you want completed:

```text
$ez Fix the failing tests in this repository.
```

ez reports the selected model, reasoning level, rationale, and confidence before delegating the work.

## Installation

Copy this directory into your Codex skills folder as `ez`:

```text
~/.codex/skills/ez/
```

Restart or reload Codex so it discovers the skill and its UI metadata.

## Structure

- `SKILL.md` - routing behavior and execution instructions
- `agents/openai.yaml` - Codex UI metadata, icon paths, and invocation policy
- `assets/` - header artwork and skill icons

The skill is configured for explicit invocation with `$ez`.
