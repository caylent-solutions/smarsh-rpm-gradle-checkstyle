# smarsh-rpm-gradle-checkstyle

RPM package providing Checkstyle plugin configuration with Google Java Style rules and Smarsh customizations.

## What This Package Does

Applies the Checkstyle Gradle plugin with a strict zero-tolerance policy (no errors, no warnings). Includes a customized Google Java Style ruleset with Smarsh-specific import ordering. Config files are symlinked to `config/checkstyle/` in the project root via manifest `<linkfile>` entries so IDEs can reference them at their conventional paths.

## Tasks Provided

| Task | Description |
|---|---|
| `checkstyleMain` | Run checkstyle on main source set |

## Configs and Assets

| File | Purpose | Synced To |
|---|---|---|
| `checkstyle.gradle` | Plugin configuration (max errors/warnings, report format) | `.packages/smarsh-rpm-gradle-checkstyle/` |
| `config/checkstyle/checkstyle.xml` | Google Java Style rules with Smarsh customizations | `.packages/smarsh-rpm-gradle-checkstyle/` and symlinked to `config/checkstyle/checkstyle.xml` |
| `config/checkstyle/suppressions.xml` | Global suppression rules | `.packages/smarsh-rpm-gradle-checkstyle/` and symlinked to `config/checkstyle/suppressions.xml` |

## Configuration

- Max errors: 0 (any error fails the build)
- Max warnings: 0 (any warning fails the build)
- Test checkstyle: disabled
- Reports: HTML only

## Rules

Based on [Google Java Style](https://google.github.io/styleguide/javaguide.html) with:
- Custom import order: `ch, com, *, org, java, javax`
- Line length: 100 characters
- Indentation: 2 spaces

## Suppressions

- `MissingJavadocType` suppressed globally
