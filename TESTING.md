# Beta testing

Thank you for trying SeZzz. This beta is intended for ordinary, non-critical
tasks. Save your work before testing; do not deliberately drain the battery,
overheat the Mac or bypass operating-system security.

## A short checklist

- Find the menu bar app and start a short Background session.
- Lock the screen, return, and check that the session continued.
- Add 30 minutes; open the end-time editor, cancel, then try applying a change.
- Stop the session and try Display On.
- Open Settings and switch languages. Check for clipped text or mixed languages.
- During an active session choose Quit and Stop. Reopen: it should be inactive.
- If relevant, try keyboard navigation, VoiceOver or a secondary display.
- For agents, follow [the setup guide](AGENTS.md), test a short authorized session,
  then verify that disabling access prevents further agent control.

## Known limitations and coverage

- Optional support payments are not included in this beta.
- An initial Claude Desktop MCP request timed out in testing; a retry passed.
  The initial delay is still under investigation.
- Broad Intel hardware, older supported macOS releases, long-duration energy,
  accessibility and all-language visual testing are not yet complete.
- The sandboxed CLI is not a general-purpose command/build wrapper.
- Notarization checks the distribution package; it is not a guarantee of
  functional correctness or an App Store review.

## Report a problem

Open an Issue with what you expected, what happened, and numbered reproduction
steps. Include app version/build, macOS version, Apple Silicon or Intel, app
language, and agent host/version if relevant. Never post passwords, access tokens,
serial numbers, private project data or unredacted diagnostics.

If SeZzz unexpectedly activates or fails to stop keeping the Mac awake, stop
using that build and report it promptly. You can quit the app; terminating its
process releases its process-owned power assertions.
