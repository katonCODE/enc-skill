# enc Skill

`enc` is a Codex skill for turning a chat or working session into a short, clear digest.

It summarizes visible, user-relevant information such as:

* what changed
* what was created
* what was decided
* important commands or outputs
* open next steps

## Install

Recommended: use Codex’s skill installer.

```text
$skill-installer
```

Then ask Codex:

```text
Install the skill from GitHub repo katonCODE/enc-skill, path enc
```

Restart Codex after installing so the skill is picked up.

## Manual install

If needed, you can install it manually:

```powershell
mkdir $env:USERPROFILE\.agents\skills -Force
git clone https://github.com/katonCODE/enc-skill.git
copy enc-skill\enc $env:USERPROFILE\.agents\skills\enc -Recurse
```

Make sure this file exists:

```text
C:\Users\<you>\.agents\skills\enc\SKILL.md
```

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
