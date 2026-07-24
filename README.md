# 4-hub — Web4 Community Hub (standalone mirror)

A single-binary Rust daemon (~6 MB) that turns a community into a sovereign
Web4 society: 7 roles, a signed machine-readable founding law, an append-only
witnessed ledger, sealed member<->hub channels, and a multi-surface API
(MCP `/tools/*`, REST `/v1`, admin web GUI).

**Start here: [`hub/README.md`](hub/README.md).**

## Layout

| Path | What it is |
|---|---|
| [`hub/`](hub/) | The hub itself: `hub-daemon`, `hub-lib`, `hub-plugin`, docs, examples |
| [`web4-core/`](web4-core/) | The Web4 core library the hub builds on (MIT-licensed) |
| [`web4-policy/`](web4-policy/) | Policy evaluation (the law gate) |
| [`web4-trust-core/`](web4-trust-core/) | T3/V3 trust tensor primitives |

## Build

```bash
cd hub && cargo build --release
```

The monorepo layout is preserved so `hub/`'s relative path dependency on
`../web4-core` resolves in this standalone clone.

## Where development happens

This repository is a **read-only mirror**, published from the
[`hub/`](https://github.com/dp-web4/web4/tree/main/hub) directory of the
[dp-web4/web4](https://github.com/dp-web4/web4) monorepo by
`scripts/publish-4-hub.sh`. History here is the filtered history of those
paths. **File issues and PRs against
[dp-web4/web4](https://github.com/dp-web4/web4).**

## License

Root [`LICENSE`](LICENSE) (AGPL-3.0-or-later) covers `hub/`;
[`web4-core/`](web4-core/) carries its own MIT license.
