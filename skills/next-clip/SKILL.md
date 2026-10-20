---
name: next-clip
description: Direct the next clip of the loaded Kagelot project from a plain-language idea, write it to the project, and propose the image renders. Use after a project is loaded and the user describes what happens next.
argument-hint: <what happens in the clip>
---

Direct the next clip of the current Kagelot project. The user's idea: `$ARGUMENTS`. If no project is loaded yet, run the load steps first (`get_kagelot_brain`, then `get_project`).

1. Log the user's instruction with `post_chat_message` so the Kagelot chat keeps the record.
2. Pick the next free clip number from the project's file tree. Never reuse a number.
3. Call `direct_clip` (1 credit) with the clip number, the user's idea and the project's locked style. Write the result with `write_project_file` to the single prompts file for that clip, as `get_kagelot_brain` describes. Every write is checked, and the new clip appears on the Kagelot canvas.
4. Propose each image asset with `create_settings_card`. Copy the prompt text from the file you wrote; never retype it. The card waits in the Kagelot chat until the user clicks Generate, so never say an image or video was made.
5. Log a short summary with `post_chat_message`, then tell the user what was written and that the cards are waiting in Kagelot.
