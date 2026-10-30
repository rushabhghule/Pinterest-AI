# Repository Standards

## One job per file

| File | Holds |
|---|---|
| `README.md` | What the project is and how to use it |
| `BOARD.md` | Allowed destinations and the old-to-new section map |
| `CLASSIFICATION_RULES.md` | The decision order and the rules |
| `CONFUSION_PREVENTION.md` | Known traps, with the rule that fixes each one |
| `WORKFLOW_PROMPT.md` | The prompt to give the AI and the output format |
| `TESTING.md` | How the rules were tested and what the results mean |
| `CHANGELOG.md` | What changed in each version |

A fact lives in one file only. Other files link to it instead of repeating it.

## Writing rules

Every rule should:

- Come from a real photo.
- Be short and have one meaning.
- Solve one problem.
- Not repeat or contradict another rule.

## When to change a rule

Change or add a rule only when:

- The AI makes the same mistake more than once.
- A board or section is added, renamed or removed.
- A new kind of photo is not covered.

Every change gets a line in `CHANGELOG.md` and a version bump.

## File names

Use `UPPER_CASE.md` names so GitHub renders every file as Markdown.
