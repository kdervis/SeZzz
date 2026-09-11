# SeZzz - Keep Mac Awake

A small macOS menu bar app for keeping your Mac awake while work continues.
Choose what stays awake, choose a duration, and get back to your task.

**Free · macOS 13 or later · Apple Silicon and Intel · Public beta**

## Download and install

**[Download SeZzz for macOS — Free Beta](https://github.com/kdervis/SeZzz/releases/download/v0.1.0-beta.3/SeZzz-0.1.0-build3-macOS.zip)**

macOS 13+ · Apple Silicon & Intel · Version 0.1.0 (3)

[Release notes](https://github.com/kdervis/SeZzz/releases/tag/v0.1.0-beta.3)

Open this repository's **Releases** section and select **SeZzz 0.1.0 Beta 3**.
Under **Assets**, download **SeZzz-0.1.0-build3-macOS.zip** — not GitHub's
automatically generated “Source code” archives.

1. Unzip the download and open the `Beta-Build3` folder.
2. Drag `SeZzz.app` into **Applications**. Quit an older SeZzz before replacing it.
3. Open SeZzz from Applications, then click **SeZzz in the menu bar**.
   There is no main application window to look for.
4. Select a mode and duration, then choose **Keep awake**.

The beta is Developer ID signed and Apple-notarized. If macOS reports a damaged
app or cannot verify it, stop and report the problem. Do not disable Gatekeeper
or remove quarantine attributes to work around it.

## Two modes, one simple menu

| Mode | What stays awake | Useful for |
| --- | --- | --- |
| Background | Your Mac; the display may sleep | Downloads, exports and long-running tasks |
| Display On | Your Mac and display | Presentations and visible dashboards |

Choose a preset duration or an end time. During a session, see the remaining
time, add 30 minutes, change the end time, or stop immediately. **Quit and Stop**
ends the session and closes the app. Normal macOS sleep settings resume afterward.

SeZzz can continue while the screen is locked; it does not unlock your Mac or
bypass its password. It does not override closing a laptop lid, explicitly
putting the Mac to sleep, or system safety decisions. Keeping a Mac awake can
increase battery use. Do not rely on a beta for unattended critical work.

## For agents and command-line users

Optional local CLI and MCP access lets compatible agents control the same
app-owned session. Nothing needs to be configured for ordinary menu bar use.

Launch the installed app, open **Agents / Agent Integrations**, explicitly enable
access, and copy the configuration for your host. See [agent setup](AGENTS.md).
Agents must use finite sessions and must not stop or replace a user's session.

## Languages

English, Turkish, German, French, Spanish, Brazilian Portuguese, Japanese,
Simplified Chinese, Korean, Russian and Arabic. Change the app language from
the menu. Translation and right-to-left layout feedback is welcome.

## Free to use

All current features are free. There is no Pro tier, subscription, advertising
or required account. This beta has **no support-payment interface**. Optional
in-app support is planned for a later release; it will not unlock features.

## Beta feedback

See the [testing checklist and known limitations](TESTING.md). Report bugs or
suggestions in this repository's **Issues** section. Include the app version,
macOS version, language, and steps to reproduce. Remove personal information
from screenshots and diagnostics before posting — GitHub Issues are public.

SeZzz does not automatically upload diagnostics or collect usage analytics.
Connecting it to an agent is optional; your chosen agent host has its own
privacy practices.

## About this repository

This is the official distribution and documentation repository for SeZzz.
It contains usage guides, feedback and downloadable releases, **not the
application source code**. GitHub's generated source archives contain only
these repository documents, not an installable app.
