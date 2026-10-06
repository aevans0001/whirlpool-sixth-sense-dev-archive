# Upstream handoff: API144 laundry controls

This branch is a temporary staging branch for contributing the validated API144 washer/dryer work back to the upstream `abmantis/whirlpool-sixth-sense` project.

It is not intended to become a separately branded or permanently maintained replacement library.

## Scope

The work on this fork includes:

- washer/dryer Start, Pause, Resume, and Cancel operations;
- read-only Remote Control Enable state;
- WFW9620HBK3 washer cycle, dispenser, Fan Fresh, Steam, and per-cycle option support;
- WED9620HBK2 dryer cycle and configuration support;
- cycle/changeability helpers needed by the Home Assistant integration;
- model-specific protocol payload handling and validation;
- supporting tests and staged payload builders.

## Important upstreaming note

The original compatibility work started from the 1.3.1-era library because that matched the live Home Assistant installation at the time.

Before opening an upstream PR, the relevant changes from this branch should be forward-ported/rebased onto the current upstream library architecture and current default branch. The goal is to contribute the functionality to the existing library, not to preserve a long-lived compatibility fork.

## Related Home Assistant work

The corresponding Home Assistant staging branch is:

`aevans0001/home-assistant-whirlpool:feature/upstream-whirlpool-laundry-controls`

Home Assistant-local Favorites, entity presentation, translations, remaining-time display, and UI/action behavior belong on the Home Assistant side. Generic Whirlpool cloud/API behavior belongs in this library.
