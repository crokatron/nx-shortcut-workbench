# NX Shortcut Workbench — visual user manual

[Project overview](../README.md) · [Offline interactive demo](../demo.html)

Start with the numbered picture guide. Each number identifies the exact highlighted control. Work through one step at a time; the longer reference is below it.

### Actual tool · controls at a glance

Actual application screenshot. Numbered boxes point to the controls described below. 

![NX Shortcut Workbench — numbered controls](images/guide-1.jpg)

1. **Search the command catalogue.** Try Extrude, then inspect the exact command identifier.
2. **Choose the output workflow.** Keyboard map, keycap printing, macropad export and side launcher are separate views.
3. **Compare matching commands.** Similar names may represent different commands or modules. Import a role before editing assignments.

### Try the working offline example

Screenshot of this project’s interactive demo. Side-by-side services are explicitly simulated.

![NX Shortcut Workbench — numbered controls](images/guide-2.jpg)

1. **Choose the command.** Use the intended command, not just a similar name.
2. **Try an assignment.** Ctrl+K is already used here. Conflicting assignments are rejected.
3. **Review the dummy role.** The new key appears in the example; your NX session is untouched.

## Detailed task reference

### Find a command

1. Type a name such as Extrude into Search all commands. Review both the displayed label and command identifier: similarly named commands can belong to different workflows.
2. Use category and installed-module filters to narrow results. Include UI controls only when you intend to inspect those entries too.
3. Open a command’s details before assigning it. Catalogue presence does not prove that your NX installation licences that command.

### Edit a role without losing the original

1. Export or copy your existing NX role first. Choose Import role and select its .mtx file. Assignment editing and Export role remain disabled until a role is available.
2. Make one assignment change, review any conflict information and use Undo change if it is not what you intended. Save a draft while working.
3. Export the edited role under a new filename, then import/test it through NX’s normal role workflow. Keep the original until you have verified the result.

### Use the companion views

1. Open Keyboard Map to inspect where assignments sit rather than reviewing only a table.
2. Use Keycap Print for physical labels/reference output and Macropad Export for the supported target format. Check the destination device/application requirements before importing it.
3. Side Launcher is a separate convenience view; browser output does not itself demonstrate successful command execution inside NX. Read Help and sources for catalogue assumptions.

## Keep your work

Keep the original .mtx, the edited export and any workbench draft separately. Browser drafts can disappear when site data is cleared. Role files and macro-pad exports are different deliverables.

## If something looks wrong

- Export disabled: import a role first.
- Missing command: widen filters and compare the command ID, module and NX version.
- NX ignores a shortcut: test the exported role in the intended NX application/context and inspect conflicts.

## What this manual does not promise

The included catalogue references NX 2412. Other versions/modules and macro hardware need testing. Siemens catalogue/icon assets retain their original rights and are not covered by the root MIT licence. This project is independent of Siemens; no additional rights to vendor assets are granted.

Screenshots show the actual application where captured. The offline demo is a deliberately smaller simulation and identifies its dummy services. It never controls devices, sends notifications, uploads files or launches printing.
