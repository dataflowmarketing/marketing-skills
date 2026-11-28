# marketing-skills

dfm (dataflow marketing) keeps a business's marketing context: how its marketing works, what it plans, what happened and how it speaks. Any AI then works from facts, not guesses.

Marketing skills for Claude from [dataflow.marketing](https://dataflow.marketing): small pieces that fit together. With them a business can keep that context, plan its marketing, make content from its own words, publish drafts and count what happened.

## Why this exists

This is based on real work I'm currently doing at [influencer.tips](https://www.influencer.tips/). It is an opportunity to share the method.

Questions are welcome: email me at matt@influencer.tips. Feel welcome to raise an [issue](https://github.com/dataflow-marketing/marketing-skills/issues). Everyone taking part follows the [code of conduct](CODE_OF_CONDUCT.md).

**Status: the first loop works: a recording becomes a checked draft post on Ghost.** The shared formats come first: [spec 1](spec/README.md) is a draft. More are being written now; [the plan](#the-plan-and-where-it-is-up-to) shows where each part is up to.

## A worked example

[The coffee shop](examples/coffee-shop/README.md) follows one made up coffee shop through a week of the loop, with its whole ledger.

## Who it is for

- **A business running its own marketing,** with Claude Code.
- **Someone running marketing for clients,** keeping each client's context in one place.

## Where to start

**Start on the [starter plan](examples/starter/README.md):** four steps a week, then change one thing at a time.

**Today, with no install:** [ask an AI about your marketing plan](docs/ask-an-ai.md). Read [a whole conversation](examples/coffee-shop/ask-ai-conversation.md) to see what comes back, paste the coffee shop's copy into ChatGPT to see it work, then make one for your own business by hand.

**When the skills are built:**

Start with a recipe. A recipe runs the skills a job needs in order and stops for a yes at each step:

- `/dfm-recipes:client-run` sets up a business: its site and its profile (a first plan comes later)
- `/dfm-recipes:week-run` brings in the week's counts and writes the summary
- `/dfm-recipes:recording-run` turns a recording into a draft post

Each skill can also be used on its own once you know what you need.

## Safety

- **No skill publishes.** Anything put on a platform is a draft; a person publishes.
- **A yes before every write.** Each write shows what would change, waits for a yes, writes and reads it back.
- **Keys never pass through Claude.** Scripts read them from a keys file named in settings.
- **No names in a ledger.** People stay in the business's own systems; a ledger holds groups and counts.
- **Nothing invented.** Content comes from the person's own words; a check proves every quote.

## Words used here

| Word | Means |
|---|---|
| context | everything an AI needs to know about a business's marketing: its ledger and its profile |
| ledger | how a business's marketing works, what it plans, what happened and a summary |
| profile | what a business says and how it says it |
| skill | one job Claude can do, such as `/dfm-ghost:post-draft` |
| piece | a skill seen as one part that fits with others |
| recipe | a skill that runs other skills in order |
| runner | what runs the skills for real people on a schedule: a member page, a scheduled job or a person in Claude Code |
| capability | what a platform skill offers, such as counts or drafts; any platform can fill it |
| connector | how a store keeps an object: a file, Ghost or a REST backend |
| scripted | a ready made function a skill runs where a guardrail is needed |
| guided | a script Claude writes for the job as it goes |
| carried | a skill whose instructions travel inside what it makes; it works in any AI chat |

## How the names work

Every skill is `dfm-<area>:<thing>-<verb>`:

- `/dfm-ghost:post-draft` puts a post on Ghost as a draft
- `/dfm-content:quotes-check` checks every quote against its source
- `/dfm-recipes:week-run` runs the weekly run

The verb says what a skill does:

| Verb | Means | Writes |
|---|---|---|
| read | fetches numbers or content | never |
| check | inspects and names problems | never |
| make | makes something new | a new file only |
| change | alters something that exists | after a yes, read back |
| record | adds lines to a ledger | yes |
| draft | puts a draft on a platform | as a draft, never published |
| add | registers a site, a key or a definition | settings |
| remove | removes something | a backup first, after an explicit yes |
| run | a recipe: several skills in order | through its skills |

## The plan and where it is up to

Everything planned, in the order it is built. Each row changes in the same commit as the work it describes.

**State:** `planned` not started | `next` being written now | `built` in the repo with its tests | `works` built and has done one real job

**Kind:** `code` a script does the work and is tested | `model` an AI model writes it from the person's own words and a check proves it | `recipe` runs other skills in order

**Script:** `yes` a script is built and committed in the skill's `dist/` folder | `no` none yet | `none` the skill needs none (guided: Claude does the job by its instructions)

**Version:** a plugin has one version for all its skills, shown in its heading. Every plugin starts at `0.x` and reaches `1.0` when spec 1 is frozen. A plugin with no built skill is `not started`.

### Build order

| Step | What | State |
|---|---|---|
| 1. spec 1 | the shared formats: ledger, words, settings, check report, store, profile, forecast | built (a draft until the first skills run on real work) |
| 2. ask an AI by hand | the instructions, the coffee shop copy and a tutorial | works |
| 3. the foundation | the workspace, `packages/core` (settings, keys, output, run log, build) and the writing check | built |
| 4. first loop | quotes-check, post-make, site-add, post-draft, recording-run | works |
| 5. ledger core | the ledger skills and week-run (first version: plan-make, plan-check, counts-record, summary-make, askai-make, week-run) | next |
| 6. the rest | content, media, storage, more platforms, upkeep | planned |

### The foundation

| Part | Does | Tests | Version | State |
|---|---|---|---|---|
| `spec/` | the shared formats every skill reads or writes | | spec 1 (draft) | built |
| `packages/core` | reads settings and keys, checks settings, makes the Ghost Admin token, formats output and the run log line, builds and checks the bundled scripts | yes, beside each file | 0.1.0 | built |
| `packages/ledger` | reads a ledger (spec 1, older words and look-alike punctuation too), carries steps forward, makes the straight line forecast; proved against real ledgers | yes, beside each file | 0.1.0 | built |
| `packages/store` | finds where an object is kept, its version (a hash of its text; a rest store's own), the Ghost member field calls, the rest calls with If-Match, the write decision, the remove, backups | yes, beside each file | 0.1.0 | built |
| `scripts/` | checks the writing rules across the repo (`pnpm check`) | yes | 0.1.0 | built |
| `examples/coffee-shop` | the made up business every test and example uses | | | built |
| `examples/starter` | the starter plan: four steps a week | | | built |
| `examples/store-worker` | a starter Hono Worker on D1 (valibot, drizzle) that meets the store contract; runs on your computer, deploys to your own account | yes, beside each file, in workerd with a local D1 | | built |
| tests on every pull request | GitHub runs the tests, the typecheck and the writing check | | | planned |

The examples have no version: they are read, never installed.

### dfm-content: words, from the person's own (0.1.0)

| Skill | Does | Kind | Script | State |
|---|---|---|---|---|
| quotes-check | checks every quote, name and number in a text against its source | code | yes | works |
| post-make | turns their own words (a transcript, notes, a reply) into a post, never invented | model | none | works |
| profile-make | makes a business's profile from its home page and /llms-full.txt (or the pages its sitemap lists); a script reads and counts the site; on a later read it keeps only the pages that changed | model | yes | works |
| share-make | words to share a post or clip on a channel, from the post's words and the person's own, checked with quotes-check | model | none | built |
| message-make | a direct message or 1:1 email from their words: short, never quoting their message back, no offer they did not make, checked with quotes-check | model | none | built |
| ideas-make | what to make next and why: the questions people asked, word for word with no one named, how often and by which group, answered on the site or by a neighbour; never writes the post | model | none | built |
| schedule-make | a run of weeks, each with its post and share | model | none | planned |
| profile-compare | what changed in a business's profile between two reads (part by part) or several businesses side by side; a script compares, Claude summarises from it | code | yes | built |
| market-read | keeps a market ledger: a business's site read the way the public sees it, read after read; code writes each read, its counts, posts, ticks and summary; also a business's ledger beside its own market ledger | code | yes | built |
| market-report | a month's market report in the same layout every month (side by side, what changed, three moves), from what profile-compare printed, checked with quotes-check | model | none | built |

### dfm-ghost: Ghost sites (0.1.0)

| Skill | Does | Kind | Script | State |
|---|---|---|---|---|
| site-add | adds a site to settings; the key goes in through a hidden prompt | code | yes | works |
| post-draft | puts a words file on Ghost as a draft and reads its status back | code | yes | works |
| numbers-read | a week's new members, paid plans started and the emails sent, their opens and clicks, also for each group by tag; read only | code | yes | works |
| said-read | what a business sent or published in a week, as said lines in its own words; read only, plan-change adds them | code | yes | built |
| fields-read | a member's custom fields | code | no | planned |
| fields-change | changes one custom field for one member: a pick list takes only its own choices; a preview, a version check, a backup, a read back; never a field that holds a ledger | code | yes | built |
| field-add | adds a custom field definition | code | no | planned |
| post-change | changes a published page's text on an explicit ask, with a backup | code | no | planned |

### dfm-ledger: the method, on any platform (0.1.0)

| Skill | Does | Kind | Script | State |
|---|---|---|---|---|
| plan-make | a first ledger: the starter plan, shaped in conversation one thing at a time, checked by plan-check | model | yes | built |
| plan-change | takes Change: lines into the ledger, each shown first, written on a yes | code | yes | works |
| plan-check | reads every line and names the problems | code | yes | works |
| counts-record | adds the counts, totals and ticks a person tells for a week | code | yes | works |
| summary-make | writes a ledger's summary: each line a want, an expectation or what happened | code | yes | works |
| askai-make | a copy of the ledger and profile for any AI chat, with its instructions inside | code | yes | built |
| askai-here | the same copy, answered by the AI the person is already in (Claude in this session): the same rounds, ending in Change: lines for plan-change | model | none | built |
| askai-send | sends the copy to an AI's API with the person's own key; the response comes back for plan-change | code | no | later |
| inbox-read | messages in become an inbox (no one named), then proposed changes through counts-record and plan-change on a yes; lists what needs a reply for message-make | model | none | built |
| followups-check | what needs following up | code | no | planned |
| rates-record | learns how well each link works from the counts | code | no | planned |
| whatif-make | what a change would bring; the forecast is kept | code | no | planned |
| people-read | counts a people list by group and state | code | no | planned |
| report-make | a short report for a period from a ledger, the same layout every time; every number from its summary or done lines, checked with quotes-check; reports, never advises | model | none | built |
| weeks-archive | past 75% of a store's limit, moves old weeks whole into the business's history; nothing lost | code | yes | built |
| spec-migrate | moves a ledger to a newer spec | code | no | planned |

### dfm-media: recordings and clips (not started)

| Skill | Does | Kind | Script | State |
|---|---|---|---|---|
| transcript-make | a recording's transcript, made on your own machine | code | no | planned |
| clips-make | clips from a recording, titled in the speaker's words | model | none | planned |
| video-encode | a copy of a clip that fits a channel's size limit | code | no | planned |
| still-make | a share card or still from a clip or post | code | no | planned |

### dfm-store: any object, in any store (0.1.0)

| Skill | Does | Kind | Script | State |
|---|---|---|---|---|
| store-add | adds a store and a binding to settings: a folder of files, Ghost member fields or a REST backend | code | yes | works |
| store-check | each binding can be read: the store answers, its key works, the member and the field are there | code | yes | works |
| objects-read | lists every object of a kind in settings: where each is and its version | code | yes | built |
| object-read | one object with its version | code | yes | works |
| object-change | changes an object only if no one else has since, a backup first, read back | code | yes | works |
| object-add | adds an object only where the place is empty, read back | code | yes | built |
| object-remove | empties an object only if no one else has changed it since, a backup first, read back | code | yes | built |

### dfm-cloudflare: site numbers from Cloudflare (started)

| Skill | Does | Kind | Script | State |
|---|---|---|---|---|
| visits-read | a week's visits, views and visits from another site, for every fact whose source is cloudflare; read only | code | yes | works |
| site-add | names a Cloudflare site, its account and its key's variable in settings | code | no | planned |
| pages-read | the most read pages | code | no | planned |
| referrers-read | where visitors came from | code | no | planned |
| token-check | which sites a token can see | code | no | planned |
| deploy-check | a Worker's live settings against its file | code | no | planned |

### dfm-stripe: sales and payment links (not started)

| Skill | Does | Kind | Script | State |
|---|---|---|---|---|
| sales-read | how many sales and subscriptions, by offer (counts, never amounts) | code | no | planned |
| link-make | a working payment link for an offer | code | no | planned |
| links-check | payment links on a site that do not take a payment | code | no | planned |

### dfm-site: any public website, read and never written to (0.1.0)

| Skill | Does | Kind | Script | State |
|---|---|---|---|---|
| site-add | adds a public website on any platform to settings, by its address only: no key | code | yes | works |
| llms-check | whether a site's `/llms.txt` is on and what it holds (title, summary, sections, links) and whether `/llms-full.txt` has every page | code | yes | built |
| links-check | links on a site that do not work for a visitor: the home page and up to 50 sitemap pages, each link asked once, politely | code | yes | built |

### dfm-social: channels with no API (not started)

| Skill | Does | Kind | Script | State |
|---|---|---|---|---|
| pack-make | a ready to post folder for a channel with no API | code | no | planned |

### dfm-recipes: the front door (0.1.0)

| Recipe | Runs, in order | State |
|---|---|---|
| recording-run | a transcript (by hand until transcript-make is built), post-make, quotes-check, post-draft | works |
| week-run | plan-check, the week's numbers (read from Cloudflare and Ghost, the rest told) and what went out, summary-make; for one business or every business bound in settings, through the store with one yes for all the writes; followups-check joins later | built |
| client-run | asks which kind of site it is (any website or Ghost), runs that site-add, then profile-make with its check, then plan-make; storing in Ghost joins later | built |
| market-run | each other business's site read for only what changed (profile-make --since), their profiles brought up to date and checked, profile-compare over time and side by side, market-report | built |
| clips-run | transcript-make, clips-make, video-encode, share-make, pack-make | planned |
| calendar-run | ideas-make, the person's answer, post-make, plan-change; schedule-make joins later | built |
| reply-run | inbox-read, then counts-record and plan-change on a yes, then message-make for each reply | built |
| report-run | summary-make, report-make, for one business or every business; rates-record joins later | built |
| review-run | whatif-make | planned |
| health-run | llms-check, links-check, profile-make (and profile-compare with an earlier read); reads only; Stripe's links-check joins later | built |
| watch-run | a scheduled read, code only (watch.sh, run by cron on the person's own computer: profile-make --since, market-read --read, a note of what changed), then in a session market-read's graph and changes and market-run's report, a yes before every write | built |

## Install

The skills' scripts need **Node 24 or later** on your PATH. With nvm, Node may only be on the PATH in an interactive shell: the skills ask how to run it when `node` is not found.

In Claude Code, add the marketplace:

```
/plugin marketplace add dataflow-marketing/marketing-skills
```

Then install every plugin at once from a terminal, in the folder you work in. `--scope local` keeps them to that folder; leave it out to have them in every session:

```
for p in dfm-recipes dfm-content dfm-ghost dfm-site dfm-ledger dfm-cloudflare; do claude plugin install "$p@dataflow-marketing" --scope local; done
```

Inside Claude Code, put `!` in front of that line to run it there. Or install one at a time with `/plugin install dfm-recipes@dataflow-marketing`.

Then start with a recipe: say "set up my business" or run `/dfm-recipes:client-run`. Settings and keys are asked for as they are needed.

## Why things are the way they are

[DECISIONS.md](DECISIONS.md). MIT licensed.

## Contributing

Pull requests are welcome; mattcam reviews each one. [CONTRIBUTING.md](CONTRIBUTING.md) says how they are accepted.
