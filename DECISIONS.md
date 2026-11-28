# Decisions

Why marketing-skills works the way it does. Each entry is a choice made over a real alternative, dated when it was first made in dataflow marketing.

## 2026-09-21: The author is mattcam
**Chose:** `mattcam` as author on every plugin, commit and manifest; mattcam reviews all of this work. Claude assists; the code review, the ownership and the thinking that guides the work come from mattcam or other contributors
**Over:** Claude as author or co-author
**Why:** "remember on the github only me is the author", then the same day "can you remove claude from the authors on this - i keep asking that"; restated for these skills: "the author should never be claude"

## 2026-10-13: Content comes from the person's own words
**Chose:** every words skill starts from the person's own words (a recording, notes, a reply), polishes them and invents nothing
**Over:** generating content and editing it into shape afterwards
**Why:** content generated first and edited later still rests on invented material; edits cannot make it the person's own

## 2026-11-02: Skills, not services
**Chose:** skills that run when someone asks, in their own Claude Code
**Over:** hosted services that run all the time
**Why:** a service has to be kept running for every user forever; a skill gives the same result with nothing to host

## 2026-11-05: Unknown until measured
**Chose:** a rate or number with no evidence behind it is shown as unknown
**Over:** reasonable guesses marked as stand ins
**Why:** a guess carried into a forecast looks like a finding; unknown keeps it honest until real counts arrive

## 2026-11-10: A week starts on Monday
**Chose:** every week runs Monday to Sunday, in the business's time zone, unless settings name another day
**Over:** each business picking its own first day
**Why:** one rule means every count, plan and summary lines up week by week

## 2026-11-11: Model the past to predict the future
**Chose:** a graph for how a business's marketing works and weekly counts for what happened; each week turns plan, do, count, summarise, change the plan
**Over:** a plan with no model behind it; a model with no counts to check it
**Why:** counts are what move a belief from assumed to proven; a forecast is only as good as the evidence it rests on

## 2026-11-11: Counts of actions, never money
**Chose:** goals and facts count actions (sign ups, sales, donations, bookings)
**Over:** revenue, prices and costs
**Why:** this is a model of how marketing works, not a financial model; counting what people do is enough to see what works

## 2026-11-11: Every belief says how sure it is
**Chose:** links and beliefs carry a strength: proven, believed, assumed or unknown
**Over:** guesses either banned or mixed in unlabelled
**Why:** a forecast built on assumptions has to say so; counts move a line from assumed to proven or show it was wrong

## 2026-11-13: No skill publishes
**Chose:** anything a skill puts on a platform is a draft; a person publishes
**Over:** skills that publish directly
**Why:** publishing puts a name on something; that decision stays with the person whose name it is

## 2026-11-18: A goal is a number a week
**Chose:** goals are written as a count over time (`want new regulars 2 a week`)
**Over:** goals with no number; a total by a date only
**Why:** a weekly number can be checked every week; a vague goal cannot be checked at all

## 2026-11-24: It keeps a business's marketing context for an AI
**Chose:** one generic structure that keeps the context of a business's marketing (how it works, what it plans, what happened and how it speaks) so an AI has what is important to work with
**Over:** a model built around the first business it was made for
**Why:** an AI given the context works from facts; without it, it guesses; the first business was an example, not the design

## 2026-11-24: Four rules for context an AI can work with
**Chose:** plain text, one record per line; every number says where it came from and how sure it is; groups, not individuals; the business's own words for things
**Over:** a structure without stated rules
**Why:** an AI reading the ledger has what matters, nothing private and nothing it needs to invent

## 2026-11-24: A summary written from the lines
**Chose:** a summary part written by a skill from the ledger's own lines, each line marked calculated, modelled or inferred
**Over:** leaving an AI to work the numbers out
**Why:** an AI asked to add up numbers can get them wrong or invent them; a calculated summary gives it the numbers

## 2026-11-24: The skill travels with the copy
**Chose:** the copy of a business's context carries its own instructions; any AI chat (ChatGPT, Gemini, the Claude app) then follows the method with nothing installed
**Over:** the method only inside Claude Code; a copy of the context with no instructions
**Why:** the people the context belongs to use whatever AI they already have; without instructions an AI reviews the format, invents numbers or drafts words that are not theirs

## 2026-11-24: An AI suggests, a person decides
**Chose:** an AI conversation ends in `Change:` lines; a person sends back the ones they want; only then is the plan changed
**Over:** an AI changing the plan directly
**Why:** the context is the business's own record of what it chose; a person in the loop keeps it that way

## 2026-11-25: The profile is summarised from the site's own text
**Chose:** a model summarises the home page and `/llms-full.txt` into fourteen parts; "how they write" is six to eight of the business's own sentences, chosen and checked word for word, never written; names, numbers, money and quotes are checked against the site; a person reads every profile and removes what is not there, never rewording it
**Over:** a short summary written freely; profiles written by hand
**Why:** an AI keeps suggestions in the business's voice only if it has their real words; a model asked to describe a site will add things the site never says

## 2026-11-25: Small pieces that fit together
**Chose:** many small skills, each with one job, that meet through shared formats
**Over:** a few large skills built around one way of working
**Why:** small pieces can be put together for businesses and scenarios nobody planned for

## 2026-11-25: Names are dfm-area:thing-verb
**Chose:** one plugin per area with a `dfm-` prefix; skills named thing then verb (`/dfm-ghost:post-draft`)
**Over:** plain names such as `content:post`; one large plugin holding everything
**Why:** the prefix avoids clashes with other plugins; one plugin per area keeps each install small; the thing first sorts related skills together

## 2026-11-25: A fixed set of verbs
**Chose:** read, check, make, change, record, draft, add, remove and run (recipes only), with a few exceptions where none fits (archive, migrate, encode, signin)
**Over:** any verb per skill
**Why:** a name can be guessed without looking it up; the verb says whether a skill writes

## 2026-11-25: Repo marketing-skills, marketplace dataflow-marketing
**Chose:** repo `dataflowmarketing/marketing-skills`, marketplace `dataflow-marketing`
**Over:** shorter names such as `skills` and `dfm`
**Why:** the long names are seen once at install, where they say what this is; the short `dfm-` names are the ones used every day

## 2026-11-25: Seven design rules
**Chose:** three layers never mixed (method, platform, recipe); skills meet through files, never calls; platform skills declare capabilities; one safety pattern for every write; words skills use a model and are checked, number skills are code; nothing personal in a skill; every format is versioned
**Over:** deciding each skill's shape as it is built
**Why:** the foundation has to hold before anything is built on it; otherwise every new scenario bends it

## 2026-11-25: What an object is and where it is kept are separate
**Chose:** skills that make an object (a ledger, a profile) know nothing about where it is stored; a binding in settings says which store holds it
**Over:** skills tied to one place, such as a particular custom field
**Why:** moving an object, adding a business or changing backend then changes one line of settings, not the skills

## 2026-11-25: Storage through connectors
**Chose:** `dfm-store` skills read and write any object through a connector: file, ghost (member custom fields) or rest (a small CRUD contract any backend can meet)
**Over:** one built in backend; a skill that builds backends
**Why:** a business keeps its data where it already is; a starter Worker that meets the contract is an example, not a skill

## 2026-11-25: Platform plugins grow by need
**Chose:** a platform's whole API fits the same thing-verb shape; a skill is added only when a real job needs it
**Over:** covering a platform's API up front
**Why:** new platform features become new skills without a new design; nothing is built that no one uses

## 2026-11-25: A model of 25 parts
**Chose:** the parts any marketing plan has to describe, including audience need, campaign, the action asked for, where someone came from, consent and assumption
**Over:** a smaller model; separate parts for customer, journey, task, KPI and strategy
**Why:** a part with nowhere to live bends some skill out of shape; the ones left out are already held by other parts

## 2026-11-25: "Came from", not "source"
**Chose:** `came from` for where a person, enquiry or sale started
**Over:** `source`
**Why:** `source` already means where a number was counted

## 2026-11-25: Want, expect and happened never mix
**Chose:** a goal (what is wanted), a forecast (what is expected) and a fact (what happened) are always kept apart; every summary line says which it is
**Over:** nothing, it was the only route
**Why:** a system that confuses what it wants, expects and gets cannot learn

## 2026-11-25: Words that read aloud
**Chose:** `when`, `every day`, `every week`, `every month`, `cycle weekly`, `removes` and `told`
**Over:** `event`, `repeat weekly:`, `remove:` and `paste`
**Why:** every word in a ledger has to be something a person would say; "paste" describes a keyboard, not where a number came from

## 2026-11-25: Four kinds of timing
**Chose:** repeat, ad hoc (a dated line), series (one step on several dates, each with its own detail) and unplanned (a record with no plan step)
**Over:** weekly steps only
**Why:** real marketing mixes routines, one offs and runs of similar but different events; a step not done in its week carries forward until done

## 2026-11-25: Spec 1 first, thin, as a draft
**Chose:** a draft spec with the formats the first skills need in full; frozen only when those skills work on real businesses
**Over:** every format written in full before any skill
**Why:** design no one has used is a guess; real use tests the spec while it is still cheap to change

## 2026-11-25: MIT licence
**Chose:** MIT
**Over:** no licence
**Why:** public skills need a licence that lets anyone use them

## 2026-11-25: Scripts, not an MCP server
**Chose:** skills ship scripts Claude runs, in Node with no dependencies
**Over:** an MCP server adding new tools
**Why:** scripts are plain files anyone can read, run anywhere Node runs and are easy to test

## 2026-11-25: Scripted where a guardrail is needed, guided everywhere else
**Chose:** scripted functions where a guardrail is required (keys, writes to a platform or store, checks, the run log); elsewhere Claude writes the script a job needs as it goes
**Over:** every step scripted; no step scripted
**Why:** a ready made function is safe where it matters; it is also faster, because it runs straight away with nothing to write or work out first; guided work stays flexible; a guided script used often is promoted to a scripted one for that speed

## 2026-11-25: Keys never pass through Claude
**Chose:** a script reads its key from the keys file named in settings
**Over:** keys passed into commands
**Why:** Claude sees what a script did, never a key

## 2026-11-25: Modular scripts
**Chose:** one job per file, a main file that reads like an outline, work kept apart from files and the network, nothing run on import, a test per module
**Over:** one script per skill doing everything
**Why:** small modules can be read, tested and reused on their own

## 2026-11-25: A shared core copied into each plugin
**Chose:** one `core/` in the repo, copied into each plugin by a script, with a test that fails if a copy differs
**Over:** plugins loading code from each other
**Why:** each plugin is installed on its own and cannot rely on another being there

## 2026-11-25: Written progressively
**Chose:** skills are written one at a time as they are needed; only working skills are listed; plugins start at 0.x
**Over:** writing every skill before anything is listed
**Why:** nobody installs something that is not there; each skill is shaped by real use

## 2026-11-25: How pull requests are accepted
**Chose:** mattcam reviews every pull request; one is merged when it is one change, follows spec 1 and the naming, scripts its guardrails, is modular and tested on the example business, holds nothing real or private, never publishes, keeps the house style and writes down its why
**Over:** accepting changes case by case with no stated rules
**Why:** contributors know before they start what will be merged; every piece added keeps fitting the others

## 2026-11-25: Scripts ready for a Cloudflare Worker, routed with Hono
**Chose:** work modules written to a Worker's limits (web standard APIs only, no state between calls, no local disk, keys passed in as values); only thin edge modules use Node; Hono, used in a highly functional way, maps work modules to routes in a Worker
**Over:** Node only scripts that would need rewriting to run at the edge; Hono inside the plugin scripts, which would need an install on every machine
**Why:** the same work can move to a Worker if and when the skills are offered as MCP tools or an API; the natural limits of an edge Worker keep modules small and stateless anyway

## 2026-11-25: The standard Worker packages, bundled (changes "Scripts, not an MCP server")
**Chose:** TypeScript with the packages a Cloudflare Worker project uses: hono, valibot with its Hono validator, jose, drizzle-orm when a store needs D1; typescript, wrangler, Worker types, vitest with the Workers pool; each script bundled into one committed file so a user needs only Node
**Over:** Node with no dependencies
**Why:** the same code then moves to a Worker without a rewrite; bundling keeps installing a plugin free of any package install; one known set keeps every plugin alike

## 2026-11-25: Vitest for tests, pnpm for packages
**Chose:** Vitest as the test framework, with `@cloudflare/vitest-pool-workers` so tests run the way a Worker runs; pnpm to install packages and run scripts (`pnpm install`, `pnpm test`, `pnpm build`)
**Over:** Node's own test runner or Jest; npm or Yarn
**Why:** Vitest is the framework Cloudflare's Worker testing pool is built on; pnpm installs fast, keeps one copy of each package on disk and is what the other dataflow marketing projects already use

## 2026-11-25: A pnpm workspace monorepo (changes "A shared core copied into each plugin")
**Chose:** one repo as a pnpm workspace: `packages/core` shared by every plugin through `workspace:*`, each plugin its own package, examples beside them; one lockfile; `pnpm -r test` and `pnpm -r build` across all
**Over:** copying the core into each plugin with a test against drift
**Why:** every script is bundled: the bundler builds the core into each plugin's `dist/` files; one lockfile keeps every plugin on the same versions; each plugin is still installed and versioned on its own

## 2026-11-25: One example business: the coffee shop
**Chose:** every example uses the coffee shop (`coffee-shop`), a made up takeaway coffee shop at coffee-shop.example, with made up people and details; a worked example follows it through one week of the loop
**Over:** a different made up business per format; real businesses
**Why:** the coffee shop has been dataflow marketing's worked example since November 2026; one business keeps examples comparable across formats; `.example` addresses can never belong to a real site

## 2026-11-25: Ask an AI works by hand before any skill
**Chose:** publish the instructions as a file to copy, a ready made copy for the coffee shop and a tutorial for making your own
**Over:** waiting for `dfm-ledger:askai-make` to be built
**Why:** the method can be tried today in any AI chat with nothing installed; the coffee shop copy tests the public instructions before a skill depends on them

## 2026-11-25: Everyone starts on the starter plan
**Chose:** one starter plan of four weekly steps (check your profiles, a new post, a post on social, reply to comments) and a goal of one more follower a week; a business then changes one thing at a time
**Over:** a blank ledger; a plan designed up front for each business
**Why:** the starter plan needs no website and no tools; every link starts unknown; the loop is how it becomes known; one change a week keeps it clear which change did what

## 2026-11-25: The forecast is a scripted function
**Chose:** a straight line through the counted weeks, worked out by code in `dfm-ledger`: the weekly number now, the likely week, rough until 8 weeks are counted and the rise needed; no date from fewer than 2 counted weeks or a line that is not rising
**Over:** an AI working it out each time; a separate forecasting service
**Why:** a forecast is a number people act on: code gives the same answer every time, can be tested and runs anywhere, even in a browser

## 2026-11-25: The skills stop at the ledger
**Chose:** skills keep and use a business's context; how ticks and numbers arrive, the page a person sees, reviewing many businesses and weekly emails belong to wherever the context lives
**Over:** skills that include a member page, email loops and review tools
**Why:** those are a product's processes, not the method; leaving them out keeps the pieces usable by any product built on the formats

## 2026-11-25: Two branches: main is what people install, develop is where work happens
**Chose:** `main` holds only finished, checked work and is the default branch people install from; `develop` takes pull requests and is merged to main when ready
**Over:** one branch for everything
**Why:** a marketplace installs from the default branch: work in progress must never land there first

## 2026-11-25: The repo starts at 0.1.0
**Chose:** a private root `package.json` at version 0.1.0 with the repo's name, description, licence, author, links, Node 24 and pnpm; workspace settings come with the first skill's code
**Over:** no `package.json` until there is code; starting at 1.0.0
**Why:** the repo's details are known now; 1.0 waits until spec 1 is frozen; `private` keeps it from ever being published to npm by mistake

## 2026-11-25: Branches are named kind/what
**Chose:** main and develop live on; every other branch is short lived, from develop, named `<kind>/<what>` in lowercase with hyphens; kinds are skill, spec, fix, docs and example
**Over:** free names; names with a person or a ticket number
**Why:** the kind says at a glance what a branch changes; the same pattern as the skill names keeps it easy to guess

## 2026-11-25: Commit and pull request titles are plain sentences
**Chose:** a title is one plain sentence saying what is now true, in sentence case, no full stop, at most 72 characters, naming the skill when there is one; commits are title only; pull requests go to develop, follow a template and are squashed
**Over:** Conventional Commits codes such as `feat:` and `fix:`; long commit bodies
**Why:** a title that reads as a sentence tells anyone what changed without a key; the why already lives in DECISIONS.md

## 2026-11-25: Releases are tagged by version
**Chose:** develop is merged to main when ready; the version goes up and main is tagged `v<version>`; 0.x until spec 1 is frozen
**Over:** releasing without versions or tags
**Why:** people installing from main can see what they have and what changed

## 2026-11-25: A code of conduct
**Chose:** a short code of conduct adapted from the Contributor Covenant 2.0: respectful disagreement about ideas, good-faith questions and owning mistakes are encouraged; harassment, trolling and sharing private information are not; reports go to matt@mattcameron.me
**Over:** no code of conduct; the full Contributor Covenant text
**Why:** people can think clearly, disagree respectfully and still feel safe; a short summary is one people read

## 2026-11-25: The GitHub organisation is dataflow-marketing (changes "Repo marketing-skills, marketplace dataflow-marketing")
**Chose:** the repo lives at `dataflow-marketing/marketing-skills`; install is `/plugin marketplace add dataflow-marketing/marketing-skills`
**Over:** `dataflowmarketing/marketing-skills`
**Why:** the organisation's name now matches the marketplace name and reads as the brand, dataflow marketing; changed before anyone installed or linked to it: nothing breaks; GitHub redirects the old address

## 2026-11-25: Pieces, not bricks
**Chose:** "pieces" for skills that fit together
**Over:** "bricks"
**Why:** read beside "dataflow", "bricks" sounds too close to Databricks

## 2026-11-25: A runner runs the pieces; the formats are the contract
**Chose:** a runner (a member page, a scheduled job or a person in Claude Code) runs the skills for real people and keeps its own processes; any runner can swap its own code for a skill one piece at a time, because both read and write the same formats
**Over:** skills that assume one way of being run
**Why:** the first runner already exists and moves onto the skills piece by piece; the same path is open to anyone else's product

## 2026-11-25: Build tools beyond the standard Worker set
**Chose:** esbuild for bundling (the version wrangler already uses) and @types/node for the Node edge files, both for development only
**Over:** only the standard Worker packages
**Why:** bundling needs esbuild; the Node edge files need their types; neither reaches someone who installs a skill

## 2026-11-25: The dist check compares content
**Chose:** build each script in memory and compare it with the committed dist file
**Over:** comparing file dates
**Why:** dates are not reliable after a fresh clone; a content match catches every stale file

## 2026-11-25: The writing check is its own workspace package
**Chose:** a `scripts/` workspace folder holding the house style check and its tests
**Over:** a loose script with no tests
**Why:** the check that guards the house style is tested like everything else

## 2026-11-25: Example settings stay word for word with the spec
**Chose:** a test that fails if the coffee shop settings used in tests differ from spec/settings.md
**Over:** separate copies that can drift
**Why:** the examples and the spec always say the same thing

## 2026-11-25: Logs are the developer's choice
**Chose:** a write is logged where the skills run, somewhere never committed but kept for reference, never holding a key; where and how is left to the developer or runner
**Over:** a log format and place fixed in the spec
**Why:** logging is a developer and operations matter; locally the logs need to exist for reference without ever being committed

## 2026-11-25: Bad settings stop a skill until resolved
**Chose:** anything in settings that would break a skill (a line that cannot be read, a missing time zone, an unknown store) stops it and names the problem; the time zone is required; weeks start on Monday unless settings say otherwise
**Over:** skipping a bad line with a warning; defaulting the time zone
**Why:** a guess could write to the wrong place or count the wrong week; it has to be resolved first

## 2026-11-26: A settings problem names the line and its kind, never the line
**Chose:** a line that is not understood is named by its number and kind ("line 3: a site line that is not understood"), never echoed
**Over:** printing the whole line back
**Why:** the most likely bad line is a key pasted into settings by mistake; keys never pass through Claude

## 2026-11-26: Nothing secret can be committed by accident
**Chose:** .gitignore holds .env files, .dev.vars files, *.log and run-log.txt
**Over:** ignoring only node_modules and .wrangler
**Why:** the repo is public; testing a skill or a Worker here makes keys files and logs that `git add .` would otherwise take

## 2026-11-26: A test sits beside the file it tests
**Chose:** each test file sits in the same folder as the code it tests, named after it with .test added (parse-settings.ts and parse-settings.test.ts)
**Over:** a separate test/ folder
**Why:** a file without a test shows at a glance

## 2026-11-26: The README shows the whole plan and where each part is up to
**Chose:** one section in the README listing every planned skill, recipe and foundation part with its state (planned, next, built, works), its kind (code, model, recipe) and whether its script is built
**Over:** listing a skill only once it works
**Why:** the whole plan and its progress are seen in one place

## 2026-11-26: The plan shows each plugin's version
**Chose:** a version column for the foundation and each plugin's version in its heading (not started until its first skill is built); the other platforms split into their own plugins in the plan
**Over:** a plan with no versions
**Why:** a plugin is installed and versioned on its own; the plan shows what someone would get

## 2026-11-26: Work stays on develop until the skills have done real work
**Chose:** every commit goes to develop; main, what people install, changes only once the skills have been applied to real work
**Over:** merging to main as each piece is built
**Why:** nothing has been tried on real work yet; main should only offer what has

## 2026-11-26: A main function reads as an outline; repeated cases become a table
**Chose:** a main function lists its steps as named calls, each step its own short function; cases of the same shape (the kinds of settings line) are a table of names and functions; every pattern carries its shape and an example line
**Over:** one loop doing several jobs and a run of near identical if blocks
**Why:** the structure shows what the code does: it can be read back and understood

## 2026-11-26: The writing check reads code and workflow files too
**Chose:** the writing check reads .ts and .yml files as well as .md, .txt and .json, skipping only the test file that holds breaks on purpose; a comma at the end of a line before a joining word on the next line is caught
**Over:** checking only the documents
**Why:** comments and messages in code are words people read; four breaks slipped into code comments on 26 Nov

## 2026-11-26: Every file in the repo is plain ASCII
**Chose:** the writing check fails any character outside plain ASCII; the ledger format writes links with `->` and taken off steps with `-`; readers still accept the Unicode arrow (U+2192) and minus sign (U+2212) from older ledgers; the coffee shop is a "cafe", without the accent
**Over:** banning only emojis and em dashes; allowing a short list of other characters
**Why:** the files stay plain text, predictable in any editor or terminal; one rule covers emojis, em dashes and symbols

## 2026-11-26: A test that needs Node is named .node.test.ts
**Chose:** a test that must run in Node (a built script run end to end, a check against node:crypto, a guard that reads files) sits beside its file as <file>.node.test.ts and runs in Node; every other test runs the way a Worker runs
**Over:** keeping such tests in a separate folder
**Why:** the rule that a test sits beside its file holds for every test; the name says where it runs

## 2026-11-26: One shared check that work modules never reach Node
**Chose:** core/build holds the one check (usesNode, nodeInWorkModules) that core and every plugin use for their guard tests
**Over:** a copy of the check in each plugin
**Why:** the copies had drifted: two still missed every "node:" import after core's was fixed

## 2026-11-26: A skill asks for what it needs; site-add asks for the time zone when it starts a settings file
**Chose:** when a skill runs and needs information it does not have, it asks for it (its script refuses until it is given); site-add takes --time-zone when it starts a new settings file and refuses to start one without it
**Over:** site-add starting a settings file with no time zone; site-add never starting one
**Why:** a skill should never leave settings that break the next skill; asking is the way to get what is missing

## 2026-11-26: The first loop works
**Chose:** mark quotes-check, post-make, site-add, post-draft and recording-run as works: on 26 Nov a real recording became a checked draft post on a real Ghost site, read back as a draft and published by no skill
**Over:** keeping them at built until the findings from that run are fixed
**Why:** a skill works when it has done one real job (spec/skills.md); the findings are fixed next, on develop

## 2026-11-26: Every yes is asked in the question dialog
**Chose:** each skill and recipe asks every question and every yes with the question dialog where there is one (options such as "Yes, go on", "Change something", "Stop"); where there is none the question is the last line of the message
**Over:** a question at the end of a message
**Why:** in the first real run a question waiting for a yes scrolled out of sight when a hook added a turn; a new user thought the skill had stopped

## 2026-11-26: Each skill says what comes next
**Chose:** every SKILL.md ends with what usually follows it; the plugin descriptions point a newcomer to dfm-recipes:recording-run
**Over:** leaving the order to the README
**Why:** a newcomer never sees the README; in the first real run nothing named the step after site-add

## 2026-11-26: post-make asks about what it cannot make out
**Chose:** a word or sentence post-make cannot make out is asked about, never cut or guessed; recording-run offers to fix a misheard transcript before post-make
**Over:** leaving out whatever it is unsure of
**Why:** in the first real run a misheard sentence was cut; it may have been the point of the post

## 2026-11-26: The quote check runs once, inside post-make
**Chose:** recording-run has four steps: transcript, post-make (which runs quotes-check and saves the passing report), site-add when needed, post-draft
**Over:** a separate quotes-check step after post-make
**Why:** in the first real run the check ran twice for the same words file

## 2026-11-26: site-add makes settings post-draft can use
**Chose:** site-add asks for the keys file (--keys-file) when settings name none and adds its line; its read back fails settings with no keys file; its key steps make the keys file readable only by the person (chmod 600)
**Over:** leaving the keys file line to be added by hand
**Why:** in the first real run post-draft refused for a missing keys file line; the keys file was also readable by other users

## 2026-11-26: A read back names the same words file
**Chose:** post-draft's read back keeps needing --words, --site and --settings with --id; the skill texts now say so
**Over:** a read back with --id alone
**Why:** the words file says which title and slug to expect; in the second real run the text said --id was enough and the read back refused

## 2026-11-26: client-run starts small: site-add, profile-make, quotes-check
**Chose:** the first client-run sets up a site and makes a checked profile; the plan (plan-make), the llms check and storing in Ghost (fields-change) join it as those skills are built
**Over:** waiting to build client-run whole with the ledger core
**Why:** both real runs showed the front door was missing; one new skill gives a newcomer a real first job now

## 2026-11-26: profile-make reads only the home page and /llms-full.txt; without it, it asks
**Chose:** profile-make reads the site's home page and /llms-full.txt, as spec/profile.md says; when /llms-full.txt is not there it stops and says how to turn it on
**Over:** reading pages another way (a sitemap, a platform's API) or text pasted in
**Why:** the spec stays as it is; a content skill never reaches into a platform; a skill asks for what it needs

## 2026-11-26: The profile is a file in the working folder for now
**Chose:** profile-make writes profile.txt in the working folder; storing it in a Ghost member field comes with fields-change
**Over:** building fields-change now to store it in Ghost straight away
**Why:** it matches the first loop (files in the working folder, Ghost only for drafts) and keeps the first client-run small

## 2026-11-26: profile-make falls back to the sitemap
**Chose:** when a site has no /llms-full.txt, profile-make asks, then reads the pages listed in the site's sitemap (up to a limit) the same way it reads the home page
**Over:** stopping until /llms-full.txt is turned on
**Why:** many sites cannot serve /llms-full.txt but almost every site has a sitemap; it still reads only the site's own public pages, never a platform's API
**Supersedes:** "profile-make reads only the home page and /llms-full.txt; without it, it asks"

## 2026-11-26: Setting up a site starts by asking its platform
**Chose:** client-run asks which platform the site is on and runs that platform's site-add; Ghost is the only platform with a plugin today, others (WordPress first) are added by demand
**Over:** a front door that assumes Ghost
**Why:** most businesses' sites are not on Ghost; the method never depends on the platform

## 2026-11-26: A generic website that dfm reads and never writes to
**Chose:** a platform for any public website, with no key and no draft skill: dfm reads it (profile-make, link checks) and never posts to it
**Over:** leaving sites on other platforms out until each has its own plugin
**Why:** any business can get a profile and checks from its site today; posting waits for its platform's plugin

## 2026-11-26: The generic website platform is called public
**Chose:** the platform word `public` in settings (`site coffee-shop: public https://coffee-shop.example`, no key) and the plugin dfm-site, whose site-add adds such a site
**Over:** `website` (reads doubled after `site`) and `web`
**Why:** it says what dfm can do with it: read what anyone can read on the public site

## 2026-11-26: Watching a site's content and voice goes on the plan
**Chose:** plan profile-compare (what changed between two profiles of a site) and watch-run (profile-make on any public site, then profile-compare, run on a schedule by a runner)
**Over:** profiling a site once only
**Why:** a public site needs no key: any business's site can be followed over time: a competitor, a peer, a client before they are one. It reads politely and profiles businesses, never private people

## 2026-11-26: client-run offers any website first, Ghost second
**Chose:** the platform question lists any website (a public site, read only) first as the start for every site; Ghost second, for a site that should also take drafts
**Over:** Ghost listed first
**Why:** most sites are not on Ghost; the generic way in comes first and a platform plugin adds to it

## 2026-11-26: The any website choice names no platforms
**Chose:** client-run describes the first choice only as "any website", never listing site builders or platforms beside it
**Over:** suggesting kinds of site (such as Squarespace or WordPress) for it
**Why:** it is for every site, whatever it is built on

## 2026-11-26: profile-make writes its counts as a file the check reads
**Chose:** profile-make's script writes the counted part to site/counted.txt beside the pages it read; the profile is checked against it as well as the site
**Over:** leaving the counted numbers to fail the check; each run inventing its own way round
**Why:** the counts are made by code and are not written on the site; in a real run the check failed on them and the session improvised this file

## 2026-11-26: dfm-ghost:site-add turns a public site into a Ghost site
**Chose:** when settings already hold a public site of the same name, dfm-ghost:site-add replaces that line with the Ghost line (the preview shows the line it replaces; the read back checks the site is named once)
**Over:** adding a second line for the same site
**Why:** every site starts as a public site; adding drafts later must not leave settings saying two things about one site

## 2026-11-26: Each choice is named by what it is
**Chose:** client-run names the choices "Any website" and "Ghost"; what each lets dfm do (read only; drafts too) is in its description
**Over:** names such as "Ghost, with drafts"
**Why:** a choice reads as what the person has, not as a feature list

## 2026-11-26: The setup skills work
**Chose:** mark profile-make, client-run and dfm-site:site-add as works: on 26 Nov they set up a real public site and made its profile, checked and approved
**Over:** keeping them at built
**Why:** a skill works when it has done one real job (spec/skills.md)

## 2026-11-26: A usual answer is offered, never chosen
**Chose:** site-add asks each question in the dialog with a usual answer (a key's variable name, the keys file) offered first as a suggestion
**Over:** choosing the answer and telling the person after ("unless you object")
**Why:** in a real run the key's variable and the keys file were picked for the person in a sentence; a skill asks, never guesses

## 2026-11-26: A capital that opens a quote is not a name
**Chose:** quotes-check skips a capital word at the start of a quote when it looks for names; the quote itself is checked whole
**Over:** reporting it as a name as well
**Why:** in a real profile it reported words such as "The" as names; the quote was already proved word for word

## 2026-11-26: The first ledger core
**Chose:** packages/ledger (the reader, carry forward and the forecast); dfm-ledger with plan-make, plan-check, summary-make, askai-make and counts-record; the week-run recipe; plan-make as client-run's third step
**Over:** a smaller first version of plan-make, plan-check and summary-make only
**Why:** with askai-make and told counts a business on any website has a plan, a weekly record and a copy for any AI; the rest (plan-change, inbox-read, followups-check, rates-record, whatif-make, picture-make) follows

## 2026-11-26: plan-make starts from the starter plan
**Chose:** plan-make begins with the starter plan (four steps a week) and changes one thing at a time in conversation
**Over:** a blank conversation
**Why:** it is how real businesses start in dfm today; it keeps the first conversation short

## 2026-11-26: Counts are told by the person in the first version
**Chose:** counts-record takes numbers the person tells it (source told); reading counts from platforms comes with their plugins
**Over:** building platform readers first
**Why:** told numbers work for every business, on any website

## 2026-11-26: The ledger is a file in the working folder for now
**Chose:** ledger.txt in the working folder, beside profile.txt; Ghost member fields later through the store skills
**Over:** storing it in a platform now
**Why:** the same reasons as the profile (simple, readable, checkable); the store comes as its own step

## 2026-11-26: Building the ledger core and swapping it into a runner are separate
**Chose:** build and prove the public ledger pieces first; swapping a runner's own code for them is its own step with its own zero difference check
**Over:** doing the first swap while building
**Why:** each step is proved on its own; a runner is never changed by a public build

## 2026-11-26: The ledger reader matches dfm's on every real field and reads plain ASCII
**Chose:** packages/ledger's reader is proved against dfm's own reader on the fields of seven real businesses, as written and again with every arrow and minus sign in ASCII: zero differences, apart from the one by design (the source paste is read as told); the grammar now stops a name at `->` as it does at the Unicode arrow
**Over:** building skills on the reader before it was proved
**Why:** a ledger written to spec 1 uses `->`; before the change a name ran on through `->` and the line could not be read

## 2026-11-26: Write plain ASCII, read the arrow and minus sign too
**Chose:** everything dfm writes uses `->` and `-`; every reader also accepts the Unicode arrow (U+2192) and minus sign (U+2212), for good
**Over:** refusing them once every ledger is in ASCII
**Why:** real ledgers already use them; AI chats write the arrow on their own. Refusing them would turn a harmless habit into an error

## 2026-11-26: The reader reads look-alike punctuation as the plain kind
**Chose:** before a ledger is read, curly quotes and apostrophes become straight ones, odd spaces (such as the no break space) become ordinary spaces and a byte order mark at the start is dropped, as the arrow and minus sign already are; everything else in a ledger is kept as written
**Over:** a line failing to read (or one name read as two) because of punctuation that looks the same
**Why:** people and AI chats paste these in; the format's own punctuation must read the same whichever kind was typed

## 2026-11-26: summary-make writes the spec's summary
**Chose:** summary-make writes the summary as spec/ledger.md and the examples show it: each line marked with its summary source and as a want, an expectation or something that happened; the straight line forecast only; this week's steps, links with a known rate, weekly numbers and their average, this week so far, link scanners and what is not counted
**Over:** matching a runner's own summary word for word, with its simulated runs
**Why:** it is what the spec promises and every line can be checked; the first version stays small. A runner that swaps to it later reads slightly differently, by design, until the forecast swap brings the simulated runs

## 2026-11-26: A topic is optional; with none it is unknown
**Chose:** a said line or words file may name a topic; with none the topic is unknown, left out of any comparison of topics, never guessed and never a topic of its own; a person can add one later; the reader reads a said line with a topic like any other and keeps the topic
**Over:** a wildcard or an empty topic; setting a said line with a topic aside
**Why:** unknown is not zero; a later skill comparing topics says how many said lines it left out

## 2026-11-26: The coffee shop example's summary is written by summary-make
**Chose:** the example ledger's summary (and the Ask an AI copy's) is the one summary-make writes from its lines: it gains this week's steps and loses a hand written not counted line that named nothing in the ledger; a test proves the example and summary-make agree
**Over:** keeping the hand written summary
**Why:** the spec says a summary is never written by hand; the example now proves it

## 2026-11-26: counts-record writes told numbers for one week at a time
**Chose:** counts-record adds a week's counts, totals (on the day told) and ticks (with when they were made, in the business's time zone); a count replaces that week's earlier count of the fact; this week's counts are so far (counted to today); a fact the graph does not declare and a step not in the week are refused
**Over:** adding a fact or step it does not know of; keeping two counts of one fact in a week
**Why:** every number is told, never guessed; the plan and graph say what can be counted (plan-check would name anything else as a problem)

## 2026-11-26: plan-make starts the file; Claude shapes it; plan-check proves it
**Chose:** plan-make's script writes the starter plan (kept word for word with examples/starter) as a new ledger starting this week, with the followers told today (none when not told); Claude then changes only what the person asks, one thing at a time; plan-check must pass
**Over:** Claude writing the whole ledger by hand
**Why:** the start is the same for everyone and is code; the shaping is a conversation; the check proves the result

## 2026-11-26: Reading and writing a text file and the time in a time zone are in core
**Chose:** core holds readText and writeText (Node edge) and nowIn (today and the time with its offset in a time zone, web standard); the ledger skills use them
**Over:** a copy in each skill
**Why:** three skills had the same copies by the time plan-make was built

## 2026-11-26: askai-make puts together the spec's copy; the summary is shared code
**Chose:** askai-make writes the copy from spec/ask-ai-instructions.txt (kept word for word), the profile and the ledger with a summary written fresh today; a test proves it makes examples/coffee-shop/ask-ai-copy.txt word for word; the summary's pieces live in packages/ledger, used by summary-make and askai-make
**Over:** askai-make running summary-make; a copy of the summary code in each skill
**Why:** skills never run each other; shared code is how two skills use one piece

## 2026-11-26: week-run and client-run's first plan
**Chose:** week-run runs plan-check, counts-record (told numbers) and summary-make, then offers askai-make; client-run gains plan-make as its third step and ends by naming week-run, askai-make and (for Ghost) recording-run
**Over:** waiting for platform readers and followups-check before week-run
**Why:** told numbers work for every business now; the readers join week-run as their plugins are built

## 2026-11-26: The Ask an AI instructions are a template; ours are the default
**Chose:** askai-make takes a template of the person's own (--instructions <file>) in place of the default instructions (spec/ask-ai-instructions.txt), filling the same blanks, {who} and {send to}, wherever they appear; the profile and the plan always follow
**Over:** one fixed set of instructions
**Why:** a business may want its own way of asking, another language or another job for the AI; the default stays the one tried with real businesses

## 2026-11-26: A goal keeps its plus as written
**Chose:** the reader keeps a goal's plus (`want followers +1 a week` as grows) and the summary shows it as written; it reads the same as without
**Over:** dropping the plus from the summary
**Why:** the summary should say the goal the way the business wrote it; a plus reads as growth

## 2026-11-26: Tests on every pull request wait until development settles
**Chose:** keep the GitHub test run (the parked ci-workflow) out for now; tests, the typecheck and the writing check run locally before each commit
**Over:** adding it now
**Why:** development is moving fast and is tested locally; the run goes in, with its actions pinned to exact versions, once things are more stable

## 2026-11-26: plan-change places, replaces or refuses; never guesses
**Chose:** plan-change reads each Change: line with the ledger's own reader to place it (done, graph, then plan); a how, ask, goal, start, fact source or link rate replaces the line before it, a step's script lines replace as a set, the rest are added; one line that is not a ledger line refuses the whole change; the shared putInPart (packages/ledger) now writes counts-record's lines too
**Over:** Claude editing the ledger by hand; writing the lines that read and skipping the rest
**Why:** a change is the person's: half a change written is harder to see than none

## 2026-11-26: Ask an AI can be answered here; an AI API comes later
**Chose:** plan askai-here, where the AI the person is already in (Claude) follows the same instructions with them and ends in Change: lines for plan-change; put askai-send (the copy sent to an AI's API with the person's own key) on the road map for later
**Over:** only a copy to paste into another AI chat
**Why:** the person is already in an AI: copying out and pasting back is a step they need not take; an API is useful too, though not yet
**Source:** stated (both options, the API for later), inferred (the reason as worded)

## 2026-11-26: askai-here is built now, as a guided skill on askai-make's copy
**Chose:** build askai-here now: no script; it makes the copy with askai-make and follows its brief with the person (rounds in the question dialog), saving the response as a new file for plan-change; for its length it uses only what is in the copy
**Over:** waiting until after the trial; a second set of instructions for here
**Why:** you asked for it now; one brief for every AI keeps what Claude does here the same as what ChatGPT does with the copy
**Source:** stated (now), inferred (the shape)

## 2026-11-26: The order to bring the skills close to the legacy method
**Chose:** the fix round from trial 4 first, then the store (dfm-store with Ghost), then counts from platforms (visits-read, numbers-read), then inbox-read for replies, then the forecast's running total and sign in
**Over:** another order, such as counts before the store
**Why:** everything the legacy method does happens in members' Ghost fields: the store closes the most distance once the skills are sound
**Source:** stated (the order), inferred (the reason as worded)

## 2026-11-26: Fixes from trial 4
**Chose:** the spec is copied into every plugin by `pnpm build` (links out of it point to GitHub, a test keeps each copy current); plan-make shapes the plan through plan-change (never by hand) and offers to put a how line that does not fit in the person's own words; the starter's wording stays as decided; askai-make suggests the person the profile names as who and dates each copy; askai-here always makes a fresh copy and numbers rounds as the brief says
**Over:** linking skills to the repo's spec/ (missing once installed); a new starter for other kinds of business
**Why:** an installed plugin has only its own folder; the starter's words were your decision: the person's own words fit it to their business instead
**Source:** inferred (from the trial findings 23 to 30)

## 2026-11-26: A Ghost field's version is a hash of its own text
**Chose:** the ghost connector's version is a hash of the field's text
**Over:** the member's `updated_at`
**Why:** `updated_at` moves when anything on the member changes (a label, another field): a write to one field would then be refused because a different one moved
**Source:** stated (agreed), inferred (the reason as worded)

## 2026-11-26: A backup before every change, not only a remove
**Chose:** every change and every remove first writes a copy into `backups/` beside the settings file, one file per write; a runner can point it elsewhere
**Over:** a backup before a remove only, as spec 1 first said
**Why:** a lost edit costs more than a small file; it matches the runner's own rule of a backup before any member's field changes
**Source:** stated (agreed), inferred (the reason as worded)

## 2026-11-26: The store never merges
**Chose:** when the version has moved, the store stops and shows both; the skill that made the change works it in again and asks again
**Over:** the store reading again and merging, as spec 1 first said
**Why:** only the skill that made an object knows how to merge it; the store keeps no knowledge of any format
**Source:** stated (agreed), inferred (the reason as worded)

## 2026-11-26: A Ghost binding names a member by email and the field
**Chose:** `binding ledger acme: members someone@acme.com next` (store, member email, field); store-check confirms exactly one member and that the field exists; with no binding an object stays a file in the working folder
**Over:** the member id; a binding being required
**Why:** an email can be read and checked by a person; keeping files as the default means nothing that works today breaks
**Source:** stated (agreed), inferred (the reason as worded)

## 2026-11-26: The first store build is file and Ghost, four skills
**Chose:** the file and ghost connectors with store-add, store-check, object-read and object-change
**Over:** the rest connector, the Worker example, objects-read, object-add and object-remove now
**Why:** that is enough to take over the write at the end of the runner's push; the rest follow
**Source:** stated (agreed), inferred (the reason as worded)

## 2026-11-26: The Ghost behaviour is proved on a test member
**Chose:** a test member on a real Ghost site to prove what Ghost does with a member write (no version check expected)
**Over:** relying on what Ghost is believed to do
**Why:** the guard at step 4 is only as good as what Ghost really does; that site already takes the trial drafts
**Source:** stated

## 2026-11-26: The store's small formats
**Chose:** the version is SHA-256 of the text in lowercase hex, `none` for an empty object; a `backups` settings line (default `backups/` beside the settings file); backups named `<kind>-<business>-<time>.txt` in the settings time zone; the place in a ghost binding is the email then the field, with no `field` word
**Over:** a shorter hash; a fixed backups folder; the `members field next` form spec 1 first showed
**Why:** a full hash needs no thought about clashes; a runner keeps its backups in its own folder; the binding reads as the agreed example
**Source:** inferred

## 2026-11-26: The backup is taken just before the write
**Chose:** object-change copies the object into the backups folder after the second read, just before writing; a preview writes nothing at all, not even a backup; an empty object is not copied
**Over:** a backup at the first read, as the spec first put it
**Why:** the copy is then exactly what the write replaces; previews that never go ahead leave no files behind
**Source:** inferred

## 2026-11-26: object-change takes the preview's version on the command line
**Chose:** `--go` needs `--version <version>`, the version the preview printed; the script reads again and stops if it differs
**Over:** the script keeping the version itself between runs; `--go` reading and writing in one step
**Why:** the yes is given to what the preview showed: the write has to prove the object is still that; a version in the command keeps the script free of hidden state
**Source:** inferred

## 2026-11-26: The store package is shared, the plugin runs it
**Chose:** `packages/store` holds the pure pieces and the Node edges (find the place, version, Ghost calls, decide the write, backups, read and write an object); `dfm-store` runs them as four skills
**Over:** the code inside the plugin only
**Why:** a runner swapping its push for the store (the next step after the reader swap) needs the same functions without a skill around them
**Source:** inferred

## 2026-11-26: The test site's Ghost is upgraded to prove the ghost connector
**Chose:** upgrade the test site's Ghost (6.58 has no member custom fields), then prove the ghost connector on a test member there
**Over:** a local Ghost at 6.71; a local copy that holds real members
**Why:** it was the agreed test site; it was found to lack member fields when checked read only
**Source:** stated (the upgrade), inferred (the reason as worded)

## 2026-11-26: The ghost connector is proved on a real member record (reverses the upgrade)
**Chose:** the business under test keeps its objects in its own member record on a Ghost site that already has member custom fields
**Over:** upgrading the test site's Ghost and keeping the test member there
**Why:** that is how the method keeps a business: as a member record; no upgrade is needed
**Source:** stated (where the data goes), inferred (the reason as worded)

## 2026-11-26: A public line beside its Ghost line is taken out
**Chose:** dfm-ghost:site-add takes out a public line when the same Ghost line is already there; it refuses two public lines of one name or a public line beside a different Ghost line
**Over:** swapping the public line for a second copy of the Ghost line; picking one of two public lines
**Why:** settings never name one site twice (finding 18); which of two lines is wrong is your call, not the script's
**Source:** inferred

## 2026-11-26: A sentence start is read from the line as written
**Chose:** quotes-check decides whether a capital starts a sentence from the line before quotes were blanked out
**Over:** a list of words never counted as names ("Its", "The", "For")
**Why:** in the trial 3 profile every one of those words followed a quote that ended a sentence; a word list would also hide a real name that is spelt like one
**Source:** inferred

## 2026-11-26: site-add suggests the key's variable from the site's name
**Chose:** the key's variable is offered as a suggestion made from the site's name (COFFEE_SHOP_GHOST_ADMIN_KEY for coffee-shop); a public site turning into Ghost asks only for what it lacks
**Over:** an example only, which left the session to pick a name and say "unless you object"
**Why:** finding 21: a usual answer is offered in the dialog, never chosen for you
**Source:** inferred

## 2026-11-26: quotes-check keeps checking one-word quotes
**Chose:** one-word quotes such as "we" or "you" stay checked
**Over:** skipping common words through a word list
**Why:** they are found in the source: extra report lines, not problems; a word list would need choosing

## 2026-11-26: objects-read lists bindings only, with no text
**Chose:** objects-read reads every binding of one kind in settings and prints each one's business, place, version and line count; an object with no binding is not listed; no object's text is printed; one that cannot be read is named and the exit code is 1
**Over:** also listing a `<kind>.txt` in the working folder; printing each object's text
**Why:** a file with no binding names no business: listing it would guess whose it is; the text is object-read's job and a list of many objects stays short
**Source:** inferred

## 2026-11-26: object-add needs no version on --go
**Chose:** `--go` alone; the place must read as version `none` at the preview and again just before the write; anything there is refused with a pointer to object-change, even the same text; an empty `--from` file is refused
**Over:** `--go --version none` to match object-change
**Why:** the only version an add can go ahead from is `none`: asking for it adds a step and proves nothing more
**Source:** inferred

## 2026-11-26: object-remove empties: a file is deleted, a Ghost field set to null
**Chose:** a remove deletes the file (a file that is already gone is no problem) or sets the member's field to null, every other field kept; `--go --version` as object-change; a backup every time; read back means version `none`; `removeObject` in packages/store/node so a runner can use it too
**Over:** writing an empty file; deleting a member
**Why:** an empty object already reads as `none` from either store; the binding names a member, never owns them
**Source:** stated (the shape in the job), inferred (the file and package details)

## 2026-11-26: spec/store.md says how a list, an add and a remove work
**Chose:** a short "List, add and remove" section in spec/store.md for the file and ghost connectors
**Over:** leaving it to the skills alone
**Why:** a runner that uses packages/store without the skills needs the same rules; the REST contract already names list, add and remove
**Source:** inferred

## 2026-11-26: object-add's go names the version none
**Chose:** `--go --version none`, as the preview prints, refused without it
**Over:** a bare `--go` for an add
**Why:** one shape for every write: a go always names the version it was shown; an add run without a preview stops
**Source:** stated (agreed), inferred (the reason as worded)

## 2026-11-26: objects-read lists bound objects only
**Chose:** objects-read lists the bindings of a kind; a working-folder file with no binding is left out
**Over:** listing an unbound `<kind>.txt` in the working folder too
**Why:** with no binding it names no business; the list is about where objects are kept

## 2026-11-26: The starter Worker's version is a new UUID on every write
**Chose:** examples/store-worker gives a random UUID as the version on each add and change; the rest connector shows and sends back whatever version a store gives, never working one out
**Over:** SHA-256 of the body, the same as the file and ghost connectors
**Why:** spec/store.md says the version changes on every write; a hash stays the same when the same text is written again or an object is removed and added again: an old If-Match could then still pass
**Source:** inferred

## 2026-11-26: The starter Worker is the parked start, moved onto drizzle
**Chose:** port the parked store-worker (Hono routes, valibot checks, the constant time key check, one SQL statement for the version check and the write) to drizzle-orm on D1, tests beside each file, an id that must be a business's name
**Over:** the parked raw SQL; starting again
**Why:** drizzle is in the standard Worker packages and you prefer it; the parked routes and tests already met the contract
**Source:** inferred

## 2026-11-26: A rest store is https, except on this computer
**Chose:** a rest store's address must be `https://`; `http://localhost` and `http://127.0.0.1` are taken for a Worker run with wrangler dev; store-add and findPlace share the one check
**Over:** any address; https only
**Why:** the store key is sent on every request and must not cross a network in plain text; trying the starter Worker on your own computer should still work
**Source:** inferred

## 2026-11-26: A rest binding's place is the object's id; store-add takes --key-name
**Chose:** `binding ledger coffee-shop: api coffee-shop` (the id is the business's name, lowercase with hyphens); `store-add --connector rest --where <address> --key-name <NAME>` writes `store api: rest <address> key in <NAME>`
**Over:** an id made up per store; the key name as part of --where
**Why:** the contract says the id is the business's name; settings already name keys by variable for sites: a rest store reads the same way
**Source:** inferred

## 2026-11-26: A missing rest object reads as none; a 409 or a 404 on a change is "moved"
**Chose:** a 404 on read is an empty object with the version `none`; the first write to it is an add (POST); a 409 on an add or a change means the object moved since it was read (as does a 404 on a change): nothing is written and object-change shows it as it is now, as when the version moved at the second read
**Over:** refusing to write an object the store does not keep yet; treating a 409 as a plain failure
**Why:** a file that is not there already reads as `none`: every connector then starts an object the same way; the store's own check at the write is the one that closes the gap Ghost leaves open
**Source:** inferred

## 2026-11-26: The write decision takes the store's limit, not its connector (changes spec/store.md notes)
**Chose:** readObject gives back the limit (none for a file, 65,535 for a Ghost field, what a rest store answers at /limits, read on every read) and decideWrite checks against it; spec/store.md now lists the answers of the contract, the 404 for a missing object and points at the starter Worker; spec/settings.md shows `key in <NAME>` on a store line
**Over:** a limit fixed per connector; reading /limits only before a write
**Why:** a rest store declares its own limit; the preview already refuses a change that is too large: it needs the limit at the first read
**Source:** inferred

## 2026-11-26: The starter Worker's kinds grow only when a real object needs them
**Chose:** the example Worker takes the four kinds spec 1 names (ledger, profile, people, forecast); a kind is added when a real object needs a rest store
**Over:** any kind at all; a longer list now
**Why:** you agreed to grow it as needed; a kind with no object behind it is guesswork
**Source:** stated

## 2026-11-26: A rest store may be on http://localhost
**Chose:** https for every rest store, except http://localhost or 127.0.0.1 for a Worker on your own computer
**Over:** https only
**Why:** a Worker run on your own computer has no certificate; nothing leaves the machine
**Source:** stated (agreed), inferred (the reason as worded)

## 2026-11-26: The rest connector covers list, add and remove too
**Chose:** object-add posts to a rest store when the object was read as missing; object-remove sends a DELETE with `If-Match`, a 404 or 409 being "moved"; each write's size check uses the store's own limit
**Over:** leaving the three newer skills to files and Ghost only
**Why:** the two branches were built side by side; one connector that works for every skill keeps the skills free of store kinds
**Source:** inferred

## 2026-11-26: A whole ask an AI conversation as an example
**Chose:** examples/coffee-shop/ask-ai-conversation.md, the coffee shop's copy pasted as it is with the AI's replies written from the copy alone, linked from the README and the tutorial
**Over:** only the copy and the tutorial's description of what comes back
**Why:** someone can see it work in principle before installing anything or pasting it themselves
**Source:** stated

## 2026-11-27: Older commit titles stay as they are
**Chose:** take names out of the files going forward and leave history alone
**Over:** rewording an older commit title and force pushing develop
**Why:** a force push gives six public commits new ids while the old commit and older file versions stay reachable; the files people read now carry no names
**Source:** stated (no force push), inferred (the reasons)

## 2026-11-27: dfm-cloudflare:visits-read comes before the other skills
**Chose:** build dfm-cloudflare:visits-read now, before the smoke test of plan-change and the rest of today's skills
**Over:** week-run asking the person for every site number until later
**Why:** the trial's week-run asked for three numbers Cloudflare already holds; "Don't know" was the only honest answer
**Source:** stated (build it first), inferred (the reason, from the trial)

## 2026-11-27: The Cloudflare account id is in the site line
**Chose:** `site <name>: cloudflare <host> account <id> key in <NAME>`: the account id in settings, only the token in the keys file
**Over:** the account id beside the token in the keys file
**Why:** the id is not a secret and one line then says everything about the site; a read-only token cannot look up its own account (Cloudflare answered "not authorized" when asked for every account)
**Source:** stated (the place), inferred (why)

## 2026-11-27: visits-read cuts the week in the business's time zone
**Chose:** ask Cloudflare by date and time, from the week's first day at 00:00 in the settings time zone
**Over:** whole UTC days, as Cloudflare keeps them
**Why:** the ledger's weeks are in the business's time zone; with UTC days a Monday morning visit in a time zone ahead of UTC lands in the week before
**Source:** stated (the choice), inferred (why)

## 2026-11-27: week-run reads the Cloudflare facts, then asks for the rest
**Chose:** in step 2, read every fact whose source is cloudflare, show the numbers, one yes records them, then ask the person only for the rest
**Over:** visits-read as a step of its own with its own yes
**Why:** one step for the week's numbers keeps the run short; the person still sees every number before it is written
**Source:** stated

## 2026-11-27: numbers-read starts with new members and email numbers
**Chose:** dfm-ghost:numbers-read reads, for a week, new members and, for the emails sent that week, sent, opens and clicks; read only, counts-record writes on a yes, as visits-read
**Over:** also paid plans started and the week's published posts in the first version
**Why:** email opens are the number most needed; the rest can come later as measures
**Source:** stated

## 2026-11-27: The person's own addresses are an own email line in settings
**Chose:** `own email: <address>`, one a line in settings, left out of new members
**Over:** a list of addresses written into the runner's code
**Why:** they are personal: settings hold everything personal
**Source:** inferred

## 2026-11-27: A Ghost measure numbers-read does not know is named, not refused
**Chose:** such a fact is printed as `not read` for the person to tell; the run goes on
**Over:** refusing the whole reading
**Why:** ledgers made before numbers-read name measures it does not read yet; one of them should not stop the email numbers coming in
**Source:** inferred

## 2026-11-27: The week's edges are shared from the ledger package
**Chose:** week-range in packages/ledger, used by visits-read and numbers-read
**Over:** a copy in each plugin
**Why:** every platform's numbers must use the same week, in the business's time zone
**Source:** inferred

## 2026-11-27: main shows the working version, tagged v0.1.0
**Chose:** merge develop into main and tag it v0.1.0
**Over:** keeping main untouched until later
**Why:** the rule was develop only until real work; the skills now run real businesses' weekly numbers: the public default branch should show them
**Source:** stated (merge, tag), inferred (why now)

## 2026-11-27: Six skills marked works, proved on real businesses
**Chose:** visits-read, numbers-read, counts-record, summary-make, plan-check and plan-change marked works
**Over:** leaving them as built
**Why:** each ran for real on 27 Nov 2026 for six businesses' ledgers kept in Ghost member fields: plan-check passed all seven ledgers (after plan-change added three unknown-rate links and changed six fact sources); visits-read and numbers-read read the week, matching the runner they replace (email numbers exactly, site numbers within the time zone edge); counts-record and summary-make wrote each ledger, then dfm-store:object-change wrote it back with a backup and a read back
**Source:** stated (mark them), inferred (the evidence)

## 2026-11-27: A step's repeat replaces its earlier repeat in plan-change
**Chose:** a step has one repeat: a Change line `every week <step> from <date>` takes the place of that step's repeat lines, matched by the step they are for, never by a prefix
**Over:** adding it beside the earlier repeat, which left the step running from the old date
**Why:** moving when a step starts (a pause until a later week) is a real change a person asks for; with two repeats the step would run from both dates
**Source:** stated (fix plan-change first), inferred (one repeat a step)

## 2026-11-27: Next builds: week-run through the store, then said-read; CI waits
**Chose:** build week-run for every business bound in settings (through the store), then dfm-ghost:said-read (what each business published in a week); CI on pull requests waits
**Over:** adding CI now that v0.1.0 is out
**Why:** your words: CI "no at this time - we wait until it is more stable"; the two builds are what the weekly run needs since the flip
**Source:** stated

## 2026-11-27: How the run for every business and said-read work
**Chose:** week-run for every business bound in settings runs each up to its preview, shows a short table, then one yes writes them all (each with its own version check, backup and read back; any can be held back); the numbers only the person can tell are asked in one question per business, "Don't know, skip" offered and never chosen for them; said-read prints its lines as Change lines that plan-change adds to done; a post is for the groups whose tag it carries, otherwise everyone
**Over:** a yes per business; skipping told numbers in the run; a new writer for said lines (counts-record --said); every post for everyone
**Why:** the shape the first run for every business took by hand on 27 Nov; plan-change already adds said lines with a preview and a read back
**Source:** stated

## 2026-11-27: Next builds: replies on the store, Ghost numbers by tag, weeks-archive
**Chose:** rewrite the reply skill onto plan-change and the store; add Ghost measures by tag to numbers-read (an audience's email numbers, paid plans started); build weeks-archive so a ledger stays under a store's size limit; the running total forecast waits
**Over:** the running total forecast now
**Why:** your words: "yes 1 and 2 and 3"; replies were the gap that could catch you out since the old push was archived
**Source:** stated

## 2026-11-27: numbers-read counts paid plans and each group by tag
**Chose:** numbers-read adds `paid plans` (paid subscriptions started in the week) and counts every email measure again for each group whose rule is a tag, from the emails whose post carries it, written `email opens [Parents]`; groups by anything else are not counted yet
**Over:** counting groups by who received each email (paid, an email address, opens), which needs every email's recipients
**Why:** the tag groups come from what numbers-read already reads; the counts match what the runner wrote before the flip, in the same form
**Source:** inferred

## 2026-11-27: weeks-archive moves old weeks whole to a history object, past 75% of the limit
**Chose:** when a ledger passes 75% of its store's limit, weeks-archive moves the done lines of all but the last 26 weeks, whole, into the business's history object (a second object bound in settings); nothing is lost and ledgers are read as before
**Over:** folding old weeks into monthly lines in the same ledger (weekly detail lost, the reader and forecast would need month lines); moving weeks at a fixed age or only on request
**Why:** stated, each a choice offered with its trade off
**Source:** stated

## 2026-11-27: A site on this computer is read like a real one
**Chose:** site-add and profile-make take http://localhost (or 127.0.0.1) with any port, as the store's rest connector already did, through one rule in core (isLocalAddress); every other address must still be https
**Over:** a special path for demo sites
**Why:** the market demo serves its made up sites on this computer; they must go through exactly the same skills as a real business
**Source:** inferred

## 2026-11-27: Next: what changed in a market, cheaply
**Chose:** build a check of which pages changed since the last read and profile-compare (over time and side by side), fix profile-make's post count and titles; prove them on a second month of the made up market demo
**Over:** the market lens and a market recipe first
**Why:** your words: "then do 1 & 2 & 3"; repeating is where the value is; these make a repeat cost a fraction of the first run
**Source:** stated

## 2026-11-27: A page with a published date is a post
**Chose:** reading a plain sitemap, profile-make counts a page as a post when it says when it was published (article:published_time; otherwise a dated time element); the counts give the first and last days posts were published
**Over:** every page in a plain sitemap counted as a page (posts: 0)
**Why:** how often a business publishes is one of the values a market comparison surfaces; most blog platforms mark a post this way
**Source:** inferred

## 2026-11-27: A later read keeps only what changed, by fingerprint
**Chose:** every read writes fingerprints.txt (a short hash of each page's title and text); a read with --since an earlier folder writes changed.txt with only the new and changed pages in full and the pages gone
**Over:** reading and rewriting every page each month
**Why:** a repeat then costs a fraction of the first run (about a third of the words in the demo's second month)
**Source:** inferred

## 2026-11-27: profile-compare is a script, Claude only summarises
**Chose:** profile-compare compares profiles part by part in code (sentences out and in; parts side by side); Claude writes the summary from what it prints
**Over:** a model comparing two profiles, as the road map first had it
**Why:** what changed must be exact and checkable; a model comparing from memory could miss or invent a change
**Source:** inferred

## 2026-11-27: Month three, a market-run recipe and a report skill before showing anyone
**Chose:** a third demo month with one twist, then a market-run recipe (read since last month, profile, compare, side by side) and a market-report skill (the same page layout every month)
**Over:** showing the two month report to a business owner as it stands and building only on their yes
**Why:** your call; a third month made by one command shows the repeat catching something new, the "regular basis" part of the pitch
**Source:** stated

## 2026-11-27: The demo's month three twist is a claim with no proof
**Chose:** in month three a cafe already in the market starts saying it was "voted the best coffee" on its street and names no vote
**Over:** a new cafe opening
**Why:** a repeat read catches a changed claim on its own; a new business is only caught once the person adds its site; it is also the problem a real client has with others' unproven claims
**Source:** inferred

## 2026-11-27: market-report is a words skill with a fixed layout, checked by quotes-check
**Chose:** market-report writes from profile-compare's output in the same layout every month (rows kept, changes marked new, three moves), with no script of its own; quotes-check proves it against the side by side, the compare and last month's report
**Over:** a script that builds the report table
**Why:** which rows tell businesses apart is a judgement; the exact part (what changed) is already a script in profile-compare
**Source:** inferred

## 2026-11-27: quotes-check needs a date whole
**Chose:** a date written year first (2026-11-28) is one number in the text and must be found whole; a source still offers its year, month and day: "since 2026" is found in a source that only has the full date
**Over:** a date read as three numbers, each found anywhere in the sources
**Why:** in the demo, 2027-01-04 passed as 2027 and 01 and 04 found on different lines; a wrong date could pass the same way
**Source:** inferred

## 2026-11-27: Each business in a market gets its own ledger like file
**Chose:** what is read about another business is kept in a ledger like file of its own, one record per line, dated, each line with its page and their words in quotes; the first read writes every line, later reads add + and - lines only; the profile stays for voice only
**Over:** the free text profile as the only record of a market, compared sentence by sentence
**Why:** your words: the ledger is "lite on free form text" with "more of a meta data approach" to "make it easy for the AI to have the required context"; "a ledger like store for each cafe would be awesome"
**Source:** stated

## 2026-11-27: A claim's proof is one of two fixed words
**Chose:** a market ledger's claim line ends `no proof on the site` or `proof on the site`; the proof itself is its own proof line
**Over:** free text after a claim ("no award named", "its awards are named")
**Why:** writing the demo by hand, a claim with "no award named" was missed by a search for claims with no proof; fixed words let a script find every one
**Source:** inferred

## 2026-11-27: The market ledger takes the ledger's own words, then market-read
**Chose:** in spec/market.md: counts as fact total lines, one said line shape with the ledger, the ledger's on word for closures (and until for an offer that ends), claim sorting marked inferred, the last part named summary; then build market-read, reading the business's own site too so its ledger can be checked against what its site says
**Over:** reshaping the market ledger into the ledger's four parts with a plan inferred from a business's posts (still open)
**Why:** your yes to "fix 2 to 6 in the spec now, since they're small and change only words. Then build market-read with 1 included"
**Source:** stated

## 2026-11-27: The market ledger is the ledger, read from outside
**Chose:** reshape spec/market.md into the ledger's four parts: graph (what stands, no dates), plan (inferred from a business's posts), done (each read, its counts, posts and what changed) and summary, with the seven improvements folded in; prove it on The Long Table by hand before market-read
**Over:** a format of its own (business, seen, now) with only the shared words aligned, as chosen earlier today
**Why:** your point: "a plan could be inferred from the past actions of the cafes"; then one format for any business and the ledger's tools read it
**Source:** stated

## 2026-11-27: quotes-check proves a market ledger's graph and done, code proves its plan and summary
**Chose:** quotes-check runs on the graph and done parts; the plan and summary are worked out by code from them and proved by its tests; a new on in done is named by its words and page, never by the dates worked out from them
**Over:** checking the whole file against the site
**Why:** on The Long Table the check rightly failed dates worked out from a post (2026-12-24, 2027-01-01) that are on no page; counts such as 7 of 9 weeks are calculated, never on the site
**Source:** inferred

## 2026-11-27: A market ledger's done lines are keyed by the read's Monday
**Chose:** every done line in a market ledger is dated by a Monday: a read and the changes it found by the Monday of the read's week (the read's own day kept on its line); a post and the step it ticks by the Monday of the week it was published, as the ledger's said lines are
**Over:** the day of the read as the key
**Why:** your words: "the cadency is weekly so it should be pinned to the monday"; the ledger keys every week by its Monday (stated); a post by its own week (inferred, from how said lines already work)
**Source:** stated, the post's week inferred

## 2026-11-27: A market ledger's plan is followed by the ledger's own ticks
**Chose:** plan lines in the ledger's plain words (every plan line is inferred, said once for the part); each post ticks its steps in the week it was published (`<Monday> <step>: done`); the summary counts the ticks and gives the strength; the dates worked out (each Monday, each date from words) are listed in a file the check reads and a person reads
**Over:** a strength note at the end of each plan line and a new missed word
**Why:** the ledger's reader skipped plan lines with a note on the end and already reads a tick; a week with no tick is already a step not done
**Source:** inferred

## 2026-11-27: profile-make keeps each post's published day in its pages file
**Chose:** a post read from a sitemap that says when it was published gets a "Published: <day>" line under its URL, read back into the post
**Over:** market-read finding a post's day in the page's text
**Why:** the day showed in the demo's text only because its pages print a time element; most sites do not
**Source:** inferred

## 2026-11-27: market-read writes a read into a new file and rewrites only what code owns
**Chose:** a read is written to a new file, never over one; --summary rewrites in place only the ticks and the summary, every other line kept as written; Claude writes the graph, the plan and what changed
**Over:** a read written over the last ledger; code writing the graph
**Why:** as profile-make never writes over an earlier read; what stands on a site and what changed are judgements in the site's words, the counts and dates are not
**Source:** inferred

## 2026-11-27: One ledger, every line with its source
**Chose:** start on one ledger format for a business seen from inside and outside: the market words and a source on every line (stated, observed, inferred; calculated in the summary) go into spec/ledger.md, a line with no source word read as stated
**Over:** two formats, the ledger and the market ledger, kept side by side
**Why:** your ask: "how do we close the gap and make them one ledger"; stated is the ledger's own word for a line that is neither observed nor inferred; your yes to step 1
**Source:** stated

## 2026-11-27: The words are defined once, in the ledger spec; outside lines wait in their own file
**Chose:** spec/ledger.md holds every word, the outside ones too, with a source last on every graph and plan line (code always writes it; no word is read as stated), a rule that keeps every line easy to grep, an offer's kind moved to after its name; spec/market.md says only how a site is read from outside; a business's own outside lines stay in a market file beside its ledger until the readers take the new words
**Over:** writing outside lines into a member's ledger now
**Why:** your question whether it would be an issue today: on a copy of a member's ledger, the reader the live page uses stopped at one outside line ("offer" is a word it does not read yet), which would break that member's page; your ask for data that is easy to select with grep
**Source:** stated (the questions), inferred (the test and the shape)

## 2026-11-27: The ledger reader learns the outside words without changing what it read before
**Chose:** the source word is taken off the end of a graph or plan line before the grammar reads it (a fact line keeps its source in its own words, as before); business, site, own, opens, offer, claim, proof, answers and channel are read by a module of their own into the graph's things; every month, every 2 weeks and on are read into the plan apart from the weekly repeats; read and new, was, gone into the done week, after a tick; the new fields are optional
**Over:** changing the grammar and the shapes every skill already uses
**Why:** every member's ledger must read exactly as before (proved on today's copies of all seven); nothing that carries a week forward should play a monthly step by mistake; a step named "new post" must stay a tick, which a test caught
**Source:** inferred

## 2026-11-27: The ledger as text, its done writer, its merges and cycles live in the ledger package
**Chose:** split and join a ledger's text, read, write and merge its done lines keeping every line as written, weekly and other cycles: moved into packages/ledger (text/) as they were, with the people and private tools taken out of their comments; a step worked out from what a business published (inferred) is marked by the reader and never counted as one of its own steps
**Over:** each page and tool keeping its own copy
**Why:** your ask that a page and the skills read and write a ledger with one set of code; the inferred guard keeps a member's page showing only the steps they plan, before any outside line goes into a member's ledger
**Source:** stated (one set of code), inferred (the guard)

## 2026-11-28: develop rewritten to take a client's words out of its history
**Chose:** fold three commits of 27 Nov into one and force push develop
**Over:** a later commit that fixed the words while the history kept them
**Why:** your yes: a comment ported from a private repo had a client's own example in it; this repo never names a client
**Source:** stated

## 2026-11-28: One summary writer; instructions for a site read from outside
**Chose:** the ledger's summary writer learns the outside lines (how often each inferred step was done, what changed, offers ended, claims with no proof), moved from market-read, which then uses it; askai-make gets a second instructions template for a site read from outside
**Over:** market-read keeping its own summary; one set of instructions for every copy
**Why:** your yes; askai-make wrote a fresh summary that dropped every outside line; its instructions told the AI the person who copied it runs that business
**Source:** stated

## 2026-11-28: Outside summary lines only on a ledger read from outside
**Chose:** the ledger's summary writer adds its outside lines only when the ledger has a read line; only steps marked inferred are counted by posts; market-read writes its summary with the ledger's writer as of the day of its last read
**Over:** outside lines on every ledger; counting a member's own steps by their posts
**Why:** a member's summary must not change (none of their ledgers has a read line); a member ticks their own steps, a post never does it for them
**Source:** inferred

## 2026-11-28: share-make and message-make next
**Chose:** build share-make (words to share a post or clip on a channel) and message-make (a direct message or one to one email from the person's own words), in the pattern of post-make
**Over:** inbox-read, member-signin or the media skills first
**Why:** your pick; both are words skills with no script, used every week
**Source:** stated

## 2026-11-28: ideas-make next, ideas as the questions people asked
**Chose:** ideas-make gives ideas whose titles are the questions people asked, word for word with no one named, each with why (how often, by which group, answered on the site or not, answered by a neighbour or not); it never writes the post
**Over:** ideas written fresh from a topic
**Why:** your yes to building it; a post stays in the person's own words, made by post-make once they answer the question
**Source:** stated (build it), inferred (the shape)

## 2026-11-28: member-signin out of scope
**Chose:** take member-signin (a sign in link for a member, to the terminal only) out of the project's plan
**Over:** keeping it planned in dfm-ghost
**Why:** your call: "descope this from the project"; no reason given
**Source:** stated (the call), the reason not given

## 2026-11-28: inbox-read next
**Chose:** build inbox-read: messages in become proposed ledger changes through counts-record and plan-change on a yes, with the messages that need a reply listed for message-make
**Over:** waiting until after Monday's tests
**Why:** your yes to building it after ideas-make
**Source:** stated

## 2026-11-28: picture-make out of scope
**Chose:** take picture-make (a ledger's flow as a diagram) out of the project's plan; review-run keeps whatif-make only
**Over:** keeping it planned
**Why:** your call: "descope this from the project"; no reason given
**Source:** stated (the call), the reason not given

## 2026-11-28: report-make after inbox-read
**Chose:** build report-make (a short report for a period) after inbox-read
**Over:** taking it out of scope with member-signin and picture-make
**Why:** your answer: "Build it"
**Source:** stated

## 2026-11-28: quotes-check needs a percentage whole
**Chose:** a percentage is one number with its sign: "6%" must be found as "6%" in a source
**Over:** its digits found anywhere in the sources
**Why:** proving report-make on the coffee shop example, an invented "up 6%" passed because the ledger has a 6 (stamp cards started)
**Source:** inferred

## 2026-11-28: whatif-make on hold
**Chose:** hold whatif-make (the simulation engine moved into the public package, with its skill and the kept forecast)
**Over:** planning it for its own session now
**Why:** your call: "lets hold off on whatif-make"; it is about one long session of work
**Source:** stated (the hold), inferred (the size)

## 2026-11-28: reply-run, report-run and calendar-run
**Chose:** build the three recipes whose skills are all built: reply-run (inbox-read, counts-record, plan-change, message-make), report-run (summary-make, report-make), calendar-run (ideas-make, post-make, plan-change)
**Over:** waiting for rates-record and schedule-make
**Why:** your yes; those join their recipes when they are built
**Source:** stated

## 2026-11-28: A scheduled run happens on the person's own computer
**Chose:** whatever runs a recipe on a schedule runs locally, on the person's own machine
**Over:** a scheduled cloud agent
**Why:** your words: "it has to run locally"; settings, keys and private market folders stay on the machine
**Source:** stated

## 2026-11-28: The scheduled read is code only, run by cron where the repos are
**Chose:** on a schedule, a script runs only the code parts of a market read (profile-make --since, market-read --read) into new folders and writes a short note of what changed; the person does the judgement later with watch-run in a session, a yes before every write; cron runs it on the computer that holds the repos
**Over:** Claude Code run unattended on a schedule; a loop inside a session; launchd on another computer
**Why:** your answers: "Code-only read" and "In the VM, with cron"; nothing unattended needs a yes, none of the subscription's limits are used
**Source:** stated

## 2026-11-28: watch.sh finds a site's last read by the day its ledger records
**Chose:** the last read of a site is the market ledger whose `read on` day is latest; each run is named for the day in the market's own time zone; a site that cannot be read is left out of that read and named in the note
**Over:** the newest folder by file time; the computer's own clock
**Why:** testing on a copy of the demo, file times picked month two over month three (copying changes them); the computer's clock is UTC, a day behind Melbourne in the morning
**Source:** inferred

## 2026-11-28: llms-check and links-check, then health-run
**Chose:** build llms-check (is a site's /llms.txt on, what it holds) and links-check (the links on a site that do not work for a visitor) in dfm-site, then the health-run recipe without its Stripe check until dfm-stripe exists
**Over:** fields-change, the media skills or schedule-make first
**Why:** your yes; two small skills unlock a whole recipe
**Source:** stated

## 2026-11-28: fields-change now
**Chose:** build dfm-ghost:fields-change (one custom field for one member, a preview first, a backup, a read back) before Monday's tests
**Over:** stopping until the tests
**Why:** your call: "yes field-change now"; inbox-read can then write a member's account answers: reply-run can then replace nudge-reply
**Source:** stated

## 2026-11-28: fields-change checks a value against the field and never touches a ledger's field
**Chose:** a pick list field takes only its own choices word for word, sent as a list ("a | b" where more than one may be picked); a text field takes text; empty clears; a field named in a binding in settings is refused (object-change changes it); the version is the hash of what the field holds; the backup and run log name the member by id, never by email
**Over:** sending whatever was asked; changing any field
**Why:** how dfm already wrote answers (pnpm answer: choices word for word, a list for a pick list); a ledger's field has its own version check and read back in object-change; the run log and backups should not hold a member's address
**Source:** inferred

## 2026-11-28: The contact email is matt@influencer.tips
**Chose:** matt@influencer.tips in the README, contributing guide, code of conduct and package.json (contact and author)
**Over:** matt@mattcameron.me
**Why:** his call: the address questions and reports go to
**Source:** stated
