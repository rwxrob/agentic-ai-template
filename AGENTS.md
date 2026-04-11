# Agent Instructions

Keep this project as agent-agnostic as possible.

## Rule: Context Maintenance

At the end of every significant task or session, summarize the current state, architectural decisions made, and pending "todo" items into AGENTS.md. Always ensure this file reflects the "ground truth" of the project so future sessions can resume without friction. Use the writeFile tool to overwrite it so the next session starts with current state.

## Rule: Commits

- Always use conventional commits (e.g. `feat:`, `fix:`, `docs:`, `chore:`)
- Never add anything agent related (copilot, claude, etc.) to commit messages or co-authorship
- Committing directly to main is okay in this repo

## Rule: Environment

- Use `/usr/bin/open` (full path) to open files or URLs on macOS — never plain `open`

## Rule: Secrets

- Never commit secrets, config files, or database files

## Rule: Code style

- Single-line paragraphs in all markdown files — no multi-line wrapped paragraphs
- Always use sentence case for titles
- No underscores or spaces in filenames; use hyphens
- No extensions on executable scripts, ever
- Run `gofmt` on all Go source files every time any change is made to Go source code
- Put all Go packages under `internal/` unless otherwise requested, to prevent external dependencies
- Prefer `go install` over `go build`
- Always use an OAuth-enabled HTTP client in Go
- In Go `bonzai.Cmd` structs, always put `Long` last so code is easier to read
- In `Cmd.Long`, indent sample/example content by 4 spaces so it renders as verbatim (preformatted) text, not markdown
- `Cmd.Short` must always be less than 50 runes
- Always add `help.Cmd` as the first bonzai subcommand

## Rule: GitHub repos

- Always enable branch protection on `main` when creating a new GitHub repo so a PR is always required
- Require zero reviews (PRs required but no approvals needed)
- Enable automatic branch deletion after a PR is merged
- After merging a PR, pull the latest changes into the current branch and delete any leftover worktrees

## Rule: Agent specific

- Always use `gh copilot` not `copilot`
- Use Claude Opus 4.6 (high) for all new projects

## Current architecture

TODO

## Current tags / versions

TODO

