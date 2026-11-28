# Contributing

Pull requests are welcome. mattcam reviews every one and decides what is merged.

For a question or an idea, [raise an issue](https://github.com/dataflow-marketing/marketing-skills/issues) or email matt@influencer.tips.

Everyone taking part follows the [code of conduct](CODE_OF_CONDUCT.md).

## Branches

- **main:** what people install. It only ever holds work that is finished and checked.
- **develop:** where work happens. Pull requests go to develop; develop is merged to main when a change is ready.
- **Everything else** is a short lived branch from develop, named `<kind>/<what>`, lowercase with hyphens:

| Kind | For | Example |
|---|---|---|
| skill | a new skill or a change to one | `skill/dfm-ghost-post-draft` |
| spec | a change to a format | `spec/forecast-kept` |
| fix | something that is wrong | `fix/quotes-check-number-words` |
| docs | the README, tutorials or guides | `docs/ask-an-ai-tutorial` |
| example | the coffee shop or the starter plan | `example/coffee-shop-second-month` |

## Commit titles

- **One plain sentence saying what is now true,** in sentence case, with no full stop: `The forecast says when a line is rough`.
- **Name the skill** when the commit is about one: `dfm-ghost:post-draft reads back the slug`.
- **Title only, no body.** The why goes in DECISIONS.md or the pull request.
- **No codes** such as `feat:` or `fix:`, no emojis, at most 72 characters.

## Pull requests

- **To develop,** never to main.
- **The title** follows the commit title rules.
- **The description** follows the [template](.github/pull_request_template.md): what changed, why and how it was checked.
- **Squashed** into one commit with the pull request's title. develop then reads as a list of changes.

## Releases

- **develop is merged to main** when a change is ready for people to install.
- **The version goes up** in `package.json` and in each changed plugin, then main is tagged `v<version>`: `v0.2.0`.
- **0.x** until spec 1 is frozen; 1.0.0 when it is.

## How a pull request is accepted

A pull request is merged when it meets all of these:

1. **One change.** One skill, one fix or one change to the spec, not several at once.
2. **It follows [spec 1](spec/README.md).** A skill reads and writes the shared formats and follows [how a skill works](spec/skills.md). A change to a format is its own pull request to the spec, made before any skill depends on it.
3. **Its name follows the pattern** `dfm-<area>:<thing>-<verb>`, with a verb from the [fixed set](README.md#how-the-names-work).
4. **Scripted where a guardrail is needed.** Anything that uses a key, writes to a platform or store or checks something is a script, never left to Claude.
5. **Modular scripts, ready for the edge.** One job per file, a main file that reads like an outline, TypeScript with only the [standard Worker packages](spec/skills.md#scripts); work modules use web standard APIs only, as [a Worker requires](spec/skills.md#ready-for-the-edge). The built `dist/` file is committed with its source.
6. **Tested.** Every module has a test with the coffee shop example, written in Vitest. `pnpm -r test` passes across the workspace. `pnpm -r build` leaves every `dist/` unchanged.
7. **Nothing real or private.** No keys, no real customer or member data, no real business in an example. Examples use the coffee shop.
8. **No skill publishes.** Anything a skill puts on a platform is a draft.
9. **The house style.** Plain words in plain ASCII. No em dashes, no emojis or other symbols, no comma before a joining word such as "and" or "but".
10. **The why is written down.** A pull request that makes a design choice adds an entry to [DECISIONS.md](DECISIONS.md): what was chosen, over what and why.

## Who owns the work

Each contributor is the author of their own commits and owns their contribution. AI assistance is fine: the person who opens the pull request has reviewed every line of it and answers for it.

By opening a pull request you agree your contribution is released under the [MIT licence](LICENSE).

## While spec 1 is a draft

The spec can still change. A pull request that depends on a part marked "to settle" may wait until that part is settled.
