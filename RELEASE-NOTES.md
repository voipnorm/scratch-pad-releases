# Scratch Pad 0.1.0 release candidate 1

First public testing candidate for the lightweight native macOS editor. The app displays 0.1.0 (build 16).

Includes tabs, independent split panes, syntax highlighting (including YAML, YANG and NETCONF/XML), Find/Replace, encoding and newline preservation, session restoration and unsaved recovery. Production builds exclude developer test tools. Hardened Runtime and App Sandbox are enabled.

**Apple Silicon only; targets macOS 14+.** Tested automatically on macOS 27.0.1; macOS 14, other hardware and remaining manual accessibility/input checks are pending. This is a prerelease, not a stable release. Automatic updates are not included.

Download the ZIP, extract it and drag Scratch Pad.app into Applications after quitting any older version. The app is Developer ID signed and Apple notarized, with its ticket stapled. The SHA-256 file verifies the ZIP download. See the README for testing limitations and recovery guidance.

Automated unit/integration, sandbox and production UI E2E checks passed; measured first-party line coverage is 90.0%. Production E2E covered save, undo/redo, search, independent split documents, crash/relaunch recovery and Save As.

Scratch Pad is MIT licensed; bundled Scintilla/Lexilla retain their upstream licenses.
