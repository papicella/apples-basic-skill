---
name: apples-basic-skill
description: >-
  Obtains the current system date and time by running the OS `date` command and
  returns the command output to the user. Use when the user asks for the
  current date, time, "what day is it", system clock, or to run `date`.
---

# Apples basic skill (current date)

## Instructions

When this skill applies:

1. Run the operating system command `date` in the terminal (from any working directory). Alternatively, from the repository root, run:
   `bash .cursor/skills/apples-basic-skill/scripts/get-date.sh`
2. Capture the command’s standard output exactly (trim only a single trailing newline if your environment adds an extra blank line when displaying).
3. Reply to the user with that output as the answer. If `date` fails, report the error output instead.

Do not fabricate a date string; always use the result of the executed command.

## Utility script

The script `scripts/get-date.sh` runs `date` with `bash` for consistent behavior. Prefer the inline `date` command when the user only needs the default system format.
