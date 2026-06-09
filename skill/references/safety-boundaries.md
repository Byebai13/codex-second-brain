# Safety Boundaries

The second brain should preserve useful context without becoming a private-data
dump or a source of false certainty.

## Never Save

- passwords
- API keys
- access tokens
- cookies
- recovery codes
- private links that grant access
- payment data
- raw account identifiers
- full chat transcripts
- private source text when the user did not ask to save it

## Do Not Treat As Confirmed Memory

- Codex guesses
- one-off user reactions
- temporary frustration
- external article claims
- advice from a source the user has not endorsed
- conclusions from incomplete evidence

Put uncertain but potentially useful items in `06-memory-candidates.md`.

## Conflict Handling

When new information disagrees with old memory:

1. Do not overwrite the old memory silently.
2. Write the conflict to `07-conflicts-and-updates.md`.
3. State the temporary handling.
4. Ask for confirmation if the conflict affects future action.

## User Confirmation

Ask for confirmation before:

- upgrading a candidate memory to a stable preference
- changing a prior decision
- replacing a project rule
- deleting or rewriting durable memory
- storing sensitive or borderline-private information

If the user explicitly instructs "remember this" or "make this my rule", still
classify the target file and avoid storing secrets.
