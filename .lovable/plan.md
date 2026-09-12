# Rebuild and repair PromptPerfect Creations

## What I’ll build
- Recreate the GitHub project in this Lovable project with its timestamped-script workflow, panel generation, retries, saved progress, and video export.
- Preserve the existing mobile-first storyboard review interface shown in the screenshots.
- Keep every Pixazo and Agnes credential in server-only secret storage; remove exposed values from copied documentation and client code.

## Image-quality repair
- Trace each timestamp from script parsing through prompt assignment and image rendering.
- Fix the repeated-bad-image path rather than merely changing seeds: validate that each panel prompt matches its own timestamp, regenerate a prompt when retrying quality, and prevent weak fallback prompts from being silently accepted.
- Reduce unsafe generation pressure so provider throttling or key contention cannot degrade results, while preserving recoverable progress.
- Add visible prompt inspection and clear failure details so a bad timestamp can be diagnosed instead of blindly rerolled.

## Technical details
- Copy the inspected TanStack Start source without repository metadata or committed credentials.
- Preserve server-only calls to Pixazo and Agnes AI, with strict input validation and bounded retries.
- Correct metadata for the app page and retain the existing design tokens.
- Verify the app at the current mobile size, test script parsing and retry interactions, and make real provider calls before declaring AI generation working.

## Security and migration checks
- Store the ten Pixazo keys and one Agnes key under environment-variable names used only by server code.
- Confirm no secret value is present in browser-delivered files or committed project text.
- No database, user accounts, or external record import were detected in the source repository.
