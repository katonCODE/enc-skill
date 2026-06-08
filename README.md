# enc Skill

`enc` is a Codex skill for turning a chat or working session into a short, clear digest.

It focuses on visible, user-relevant information: what changed, what was created, what was decided, important commands or outputs, and open next steps.

## Install

After this repository is published on GitHub, install the skill with:

```powershell
python C:\Users\%USERNAME%\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py --repo OWNER/REPO --path enc
```

Replace `OWNER/REPO` with the GitHub repository path.

Restart Codex after installing so the skill is picked up.

## Use

Ask Codex to use the skill:

```text
use enc
```

or:

```text
summarize this chat
```

## Contents

The skill lives in `enc/SKILL.md`.
