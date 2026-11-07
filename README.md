# opt-storage

Settings storage page for **OPT**, a performance mod for Deadlock. The mod loads
https://gfkm.github.io/opt-storage/ in a hidden in-game browser panel and keeps one
`localStorage` record (`opt.settings.v1`): the settings the player changed in OPT's rows,
so they survive a game restart. The page sends nothing anywhere and stores nothing else.

Protocol: request `#opt1.<id>.<op>[.<base64url payload>]` (`get` | `set` | `del`), answer in
the page title, `OPT1:` + JSON `{id, ok, op, value?, err?}`.

Source of truth: the OPT repository, `web/opt-storage/`. Edit there and redeploy; do not edit here.
