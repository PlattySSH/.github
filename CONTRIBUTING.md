# Contributing to Platty

Thanks for helping out. Bug reports, ideas, docs fixes and code are all welcome.

## Before you start

- **Bugs and ideas** go in [issues](https://github.com/PlattySSH/platty/issues/new/choose). Search first; a 👍 on an existing issue helps us prioritize.
- **Security issues** must be reported privately. See [SECURITY.md](SECURITY.md).
- **Bigger changes**: open an issue to talk about it before writing the code, so your time isn't spent on something that won't fit.

## Where the code lives

Everything is developed in [PlattySSH/platty](https://github.com/PlattySSH/platty). The libraries [vt](https://github.com/PlattySSH/vt), [pty](https://github.com/PlattySSH/pty) and [glyphs](https://github.com/PlattySSH/glyphs) are published from its `libs/` folder, so send pull requests for them to the `platty` repository too. The website and docs live in [plattyssh.github.io](https://github.com/PlattySSH/plattyssh.github.io).

## Building

You need Windows and Go 1.26 or later.

```sh
git clone https://github.com/PlattySSH/platty
cd platty
go build -ldflags "-H windowsgui" -o bin/platty.exe ./cmd/platty
```

Before opening a pull request, make sure these pass:

```sh
go vet ./...
go build ./cmd/platty
```

For UI changes, `go run ./cmd/platty-preview -o shots` renders every screen to PNG without opening a window. Add a before and after screenshot to the pull request.

## Code style

- No comments in the code. Names and small functions should explain it.
- Guard clauses and early returns; no `else` after a `return`.
- A blank line between a call and its `if err != nil`, and around `if`, `for`, `switch` and `select` blocks.
- Imports in three groups: standard library, external modules, this module.
- Constants at the top of the file, no magic strings.
- Logic that isn't UI goes in its own package under `internal/`, not in `internal/app`.
- Format with `gofmt`.

## Text

Everything in the repository is in English: UI strings, docs, commit messages and file names. Write plain, friendly sentences and keep jargon out of the UI.

## Commits and pull requests

- Branch from `main` and name the branch `type/short-description`, for example `fix/sftp-rename`.
- Commit messages follow [Conventional Commits](https://www.conventionalcommits.org) on a single line, in the imperative, under 72 characters: `fix(sftp): keep the selection after a rename`.
- Types: `feat`, `fix`, `refactor`, `perf`, `docs`, `style`, `chore`, `ci`, `build`. The scope is the area you touched: `sftp`, `vault`, `vt`, `termview`...
- One commit, one change. If it doesn't fit in one line, it's probably two commits.
- Use the same format for the pull request title.

## License

By contributing, you agree that your work is released under the [MIT License](https://github.com/PlattySSH/platty/blob/main/LICENSE).
