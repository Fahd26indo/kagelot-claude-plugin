---
name: load
description: Open a Kagelot film project from its board link or id and get ready to direct. Use when the user pastes a kagelot.com project link or says "load this project".
argument-hint: <project link or id>
---

Open the Kagelot project in `$ARGUMENTS`. If no link or id was given, call `list_projects` and ask which one.

1. Call `get_kagelot_brain` once per session and follow it. It is the operating guide for how a Kagelot project is laid out.
2. Call `get_project` with the link or id. Read `memory.md` in full: it holds the locked style, the approved characters and where the story stands. Trust it over anything you remember.
3. Read the screenplay and the most recent clip's prompts file with `read_project_file`, so the next clip continues the story.
4. Reply in a few lines: the project name, the locked style, the main characters, the last clip written, and what the next clip should be. Then ask if the user wants you to direct it.

Never redescribe an approved character's look in a prompt, and never change the locked style without asking.
