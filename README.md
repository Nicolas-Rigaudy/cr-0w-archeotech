# cr-0w-archeotech

A [CR-0W](https://github.com/Nicolas-Rigaudy/cr-0w) brick for the [archeotech shell](https://github.com/Nicolas-Rigaudy/archeotech-shell): two bar and panel modules that show crow's state on the desktop.

- `crow-agents/`: background run slots, agents working or waiting, finished runs, with toasts.
- `crow-usage/`: account usage gauges (5h and weekly windows) and costs.

Each folder has its own README with the config keys.

## Install

```sh
crow modules add https://github.com/Nicolas-Rigaudy/cr-0w-archeotech
crow archeotech link
```

`add` clones the brick into the CR-0W modules dir and pins the newest tag in `modules.lock`.
`link` symlinks both modules into `~/.local/share/archeotech/modules` (or `$ARCHEOTECH_MODULES_DIR`).
Then add `plugin:crow-agents` and `plugin:crow-usage` to your shell bar layout.

Update with `crow modules update cr-0w-archeotech`. The symlinks point at the clone, so they follow.
Remove with `crow archeotech unlink`, then `crow modules remove cr-0w-archeotech`.

## Develop

`runbooks/` covers fixtures, headless renders and the shell's gotchas.
Lint: `/usr/lib/qt6/bin/qmllint crow-agents/*.qml crow-usage/*.qml`.

## License

MIT, see `LICENSE`.
