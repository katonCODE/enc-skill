# enc Skill

`enc` is a Codex skill for turning a chat or working session into a short, clear digest.

It focuses on visible, user-relevant information:

* what changed
* what was created
* what was decided
* important commands or outputs
* open next steps

## Install

### Recommended: Codex skill installer

In Codex, run:

```text
$skill-installer
```

Then ask:

```text
Install the skill from GitHub repo katonCODE/enc-skill, path enc
```

Restart Codex after installing so the skill is picked up.

## Manual global install

Codex global user skills are stored in:

```text
$HOME/.agents/skills
```

### Windows PowerShell

```powershell
$dest = "$HOME\.agents\skills\enc"
$tmp = "$env:TEMP\enc-skill"

Remove-Item $tmp -Recurse -Force -ErrorAction SilentlyContinue
Remove-Item $dest -Recurse -Force -ErrorAction SilentlyContinue

git clone --depth 1 https://github.com/katonCODE/enc-skill.git $tmp
New-Item -ItemType Directory -Force "$HOME\.agents\skills" | Out-Null
Copy-Item "$tmp\enc" $dest -Recurse -Force

Test-Path "$dest\SKILL.md"
```

### macOS / Linux

```bash
DEST="$HOME/.agents/skills/enc"
TMP="/tmp/enc-skill"

rm -rf "$TMP" "$DEST"

git clone --depth 1 https://github.com/katonCODE/enc-skill.git "$TMP"
mkdir -p "$HOME/.agents/skills"
cp -R "$TMP/enc" "$DEST"

test -f "$DEST/SKILL.md"
```

Restart Codex after installing if the skill does not appear.

## Use

Ask Codex:

```text
use enc
```

or:

```text
summarize this chat
```

## Contents

The skill lives in:

```text
enc/SKILL.md
```
