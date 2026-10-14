# NX Shortcut Workbench: maintainer handover

[One-screen summary](START-HERE.md) · [User manual](USER-MANUAL.md) · [Feature overview](../README.md) · [Recorded validation](../VALIDATION.md)

## Purpose and behaviour to preserve

Browse an NX command catalogue, inspect command identifiers and work with shortcut assignments from an imported role. Additional views help arrange keyboard references, keycap printing, macropad output and a side launcher. Editing here does not automatically change the active Siemens NX session.

- **Search and categories:** Find commands, filter by installed-module grouping and show assignments or UI controls. (Workbench views.)
- **Role import/export:** Import an .mtx role before editing assignments; export the resulting role for NX. (Workbench views.)
- **Draft and undo:** Save an editing draft and undo changes in the workbench. (Workbench views.)
- **Keyboard Map:** Review assignments spatially on a keyboard. (Workbench views.)
- **Keycap Print and Macropad Export:** Prepare reference/key-label output and supported macro-pad data. (Workbench views.)
- **Side Launcher and help:** Review launcher options and the documented catalogue sources. (Workbench views.)

The [demo](../demo.html) is a smaller, labelled simulation with fictional data. It explains cause and effect without the real service; it is not evidence of a working production installation. Numbered screenshots in the user manual distinguish actual-app captures from demo captures.

## Files and sources of truth

| Actual package path | Maintainer role |
| --- | --- |
| [external-sources/StandaloneTools/NX-Shortcut-Workbench.html](../external-sources/StandaloneTools/NX-Shortcut-Workbench.html) | Single-file editor, command catalogue and embedded assets |
| [demo-source](../demo-source) | Editable demo HTML/CSS/runtime and embedded screenshot tour |
| [SOURCE-MANIFEST.json](../SOURCE-MANIFEST.json) | Original copied-source paths and SHA-256 checkpoint values |

The original working source is under C:/Users/lamon/Desktop/AI TOOLS/NAS for NAS modules; adjacent CAD/watch source locations are recorded by the full backup’s reviewed source manifest. This package contains only the explicitly copied source, not an automatic mirror. The main private nas-projects backup retains the broader shared host context.

## Setup, run and tests

Run commands from this repository root unless a `cd` is shown. Use a disposable checkout and fictional data for first setup. Dependencies, SDKs, signing material and personal data are not bundled. The following are continuation instructions grounded in the retained source, **not commands executed or newly certified by this handover**.

```powershell
python -m http.server 8765 --bind 127.0.0.1
```

/external-sources/StandaloneTools/NX-Shortcut-Workbench.html

Selected project check:

No independent automated production test suite is included for this module/single-file package. Use the project-specific checks below and the shared host test suite where applicable; do not invent an `npm test` command.

For the documentation demo alone, serve this repository on loopback with `python -m http.server 8765 --bind 127.0.0.1` and open `/demo.html`. Choose a free port if another preview is running. JavaScript syntax can be checked with `node --check demo-source/runtime.js`. `python demo-source/rebuild.py` rewrites demo.html, so run it only in a disposable checkout or an authorised demo-editing session. A local server cannot provide missing HA/CAD/NAS functions. Inspect browser tests for installed dependencies, fixture requirements and network targets before running them with the approved browser tooling.

## Data, configuration and backup boundaries

Preserve the original .mtx, edited export and browser draft separately. No command applies changes to a running NX session automatically. Catalogue/icon data references NX 2412 and needs redistribution rights review.

Keep the original .mtx, the edited export and any workbench draft separately. Browser drafts can disappear when site data is cleared. Role files and macro-pad exports are different deliverables.

Git preserves reviewed source and documentation. It does not copy browser storage, application databases, uploaded models/photos, accepted device settings, SDKs or credentials. Maintain independent recovery copies of the data identified above, including matching configuration and asset versions. Never add real secrets to examples, issues or logs. Private source copies on GitHub are not proof of a complete NAS/offsite data backup.

## Current verification and Git state

Before these documentation edits on 14 October 2026, this package was clean on branch `main` at `768daa9e214e4e60827af319b8e481f54ec9bf39` and its private upload was verified. All 1 manifest-listed source entries matched their stored checksums before editing. The upload follow-up has completed all 17 repositories and is paused; it does not run this tool or back up its live data.

These handover pages and README links accompany the private source package. Preserve them when continuing; stage only reviewed changes. Recheck current `git status --short --branch` and `git diff` before starting. No project-specific background schedule was inspected or changed in this documentation pass. Any service schedules in older notes are historical claims to verify in the actual deployment.

Earlier package checks and limits are recorded in [VALIDATION.md](../VALIDATION.md). This handover adds documentation/link/whitespace/secret and source-preservation checks only. No current NAS release, real hardware state, fresh installation, complete data restoration or offsite-backup freshness was verified here.

## Recovery approach

1. Preserve the current installation/data before changing it. Identify the exact code commit and data snapshot required; do not assume this package matches the running service.
2. Recover source into a new folder. Verify the source manifest and restore the project-specific configuration/assets described above separately. Recreate dependencies from the retained project files and guides.
3. Restore user data into an isolated instance or clean test browser. Check a representative editable record, associated files and save/reload behaviour, then compare to the original. Do not test recovery by overwriting production.
4. Record what actually restored and what remains missing. A demo opening or a passing syntax check is not a production recovery drill. Real deployment/device actions need the existing authorised workflow.

## Known limits and next work

The included catalogue references NX 2412. Other versions/modules and macro hardware need testing. Siemens catalogue/icon assets require rights review before public distribution; the repository remains private.

**Priority:** Round-trip a copied role and verify command IDs/conflicts in the intended NX version and modules. Test macro-pad output on its actual firmware; keep existing roles recoverable and the repository private pending asset review.

Common symptoms to check for this tool:

- Export disabled: import a role first.
- Missing command: widen filters and compare the command ID, module and NX version.
- NX ignores a shortcut: test the exported role in the intended NX application/context and inspect conflicts.

Keep [the release checklist](../RELEASE-CHECKLIST.md) and [third-party notes](../THIRD-PARTY.md) with the package. Original contributions use MIT; bundled/upstream code and assets keep their own licences. Public publication is a separate decision; preparing documentation is not permission to publish.
