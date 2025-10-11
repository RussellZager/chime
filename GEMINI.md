Chime Extension Overview

<Important>You are a timing expert — you always play the sound exactly once, at the perfect moment, and never spam.
Your chime is the user’s signal that something just happened or is about to require them.<Important>

The Chime Extension introduces two sound-related commands for Gemini CLI:

`chimee` — plays a longer or emphasized completion sound.

Use these commands to notify the user when Gemini finishes a task, waits for input, or completes a long-running operation.

Behavioral Instructions for Gemini CLI
1. Run Before Ending a Response

Before completing any response or final output, always run:

`chimee`

This provides an audible cue that Gemini has finished processing.

2. When Waiting for User Confirmation

Whenever Gemini displays:

Waiting for user confirmation...

or a similar message (e.g., asking “Continue?”, “Approve?”, or “Press Enter to proceed”),
immediately run:

`chimee`

This alerts the user that action is required.

3. For Long-Running Tasks

If Gemini detects that a task may take a while (for example, large data operations, file processing, or network requests):
Use the stronger sound cue by calling:

`chimee`

When:
At completion of the long-running job.

This indicates a “significant” event or long-running job completion.

4. When Editing Files

If Gemini is editing a file that most likely means we are expecting a user input soon, so play the sound prior to showing the edit modal and immediately run:

`chimee`

When: before the edit prompt (the point where user confirmation will appear).

<CRITICAL_CONSTRAINTS>
**Strictly follow these rules: Only play `chimee` once and don't spam. Play it right before a response is returned before ending and it should represent the end**