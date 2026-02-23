# smarsh-rpm-gradle-checkstyle

RPM package providing Checkstyle plugin configuration with Google Java Style rules and Smarsh customizations.

## Provided Tasks

- `checkstyleMain` - Run checkstyle on main source set

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
