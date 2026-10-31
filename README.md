# Scratch Pad

A lightweight native macOS text editor with a dark interface, tabs, independent split panes, syntax highlighting, Find/Replace, and session and unsaved-draft recovery. Formats include YAML, YANG and NETCONF/XML.

This is the public distribution repository for Scratch Pad. Application source is maintained separately; this repository contains download information, release notes and licenses.

## Download and install

[Download the 0.1.0 release candidate](https://github.com/voipnorm/scratch-pad-releases/releases/tag/v0.1.0-rc.1).

- Requires an Apple Silicon Mac. Intel builds are not available.
- Targets macOS 14 or later. Automated validation ran on macOS 27.0.1; macOS 14 and other hardware validation remain pending.
- Download `ScratchPad-0.1.0-arm64.zip`, extract it, and drag **Scratch Pad.app** to **Applications**. Quit an older running version first, then open the installed app.
- The app is Developer ID signed, Apple notarized, and has a stapled notarization ticket. No security settings need to be disabled.
- Automatic updates are not yet implemented; download updates here manually.

Optional download integrity check: download the matching `.sha256` file into the same folder and run:

```sh
shasum -a 256 -c ScratchPad-0.1.0-arm64.zip.sha256
```

## Release candidate status

This is a prerelease for testing, not a stable release. The app reports version **0.1.0**, build **16**; the distribution tag is **v0.1.0-rc.1**.

Unit/integration tests, sandbox checks, coverage gates, and external production UI tests passed. Measured first-party line coverage was 90.0% overall (Core 95.2%, native editor bridge 93.2%, App 83.8%). UI tests exercised editing and saving, undo/redo, search, independent split documents, crash recovery, layout restoration and Save As.

Manual VoiceOver, physical input methods, large-file scrolling, clean-Mac installation and supported-OS checks remain pending. Please keep backups of important files during prerelease testing. Older authorization bookmarks may restore as recovered copies after a signing change; reopen the original or use Save As. Do not delete recovery folders to troubleshoot unsaved work.

Documents are handled as text, with no document script execution. The app uses Hardened Runtime and App Sandbox; these protections do not guarantee the absence of vulnerabilities.

## Feedback

[Report a bug](https://github.com/voipnorm/scratch-pad-releases/issues) with the app version, macOS version, steps to reproduce and expected behavior. Avoid attaching passwords, private documents or other sensitive information.

## License

Scratch Pad first-party software and this repository's documentation are distributed under the [MIT License](LICENSE), copyright Christopher Norman. Third-party Scintilla and Lexilla components retain their own permissive licenses; see [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md) and the license files bundled inside the app.
