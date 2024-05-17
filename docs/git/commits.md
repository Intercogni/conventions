# GitHub
This document outlines all the conventions to adhere when using git commits

## TLDR
> Git commit message format:
> `<type>(<scope (optional)>): <message in present tense>`

`<type>`:
- `feat`: for all feature addition and changes in implementation
    > Example: `feat: add about page`
- `fix`: for all feature fix and debug efforts
    > Example: `fix(about): fix profile picture div centering issue`
- `refactor`: for all work which includes a change in code structure but not a change in implementation
    > Example: `refactor(projects): change every (<creator>_<project_name>) variable name into (<project_name>_<creator>)`
- `docs`: for all changes or updates in documentation
    > Example: `docs(about/readme.md): add subchapter: 'rules for adding new projects'`
- `style`: for all work which includes a change in code look/style but not a change in implementation
    > Example: `style(*.tsx): remove semicolons for all typescript react files for ease-of-reading`
- `chore`: for all grunt/houseworking tasks that does not neatly fall into either `refactor`/`docs`/`style`/`test`
    > Example: `chore: change from npm to pnpm for better performance`