# Artem Trofymenko

**Business Operations · AI Workflow Automation & Internal Tools**

<p align="center">
  <img src="assets/built-for-the-messy-reality.gif" width="420" alt="A tidy three-step system, context, build, verify, meets a piece that does not fit and is rebuilt around it. Built for the messy reality.">
</p>

I spent around 20 years running B2B businesses as a founder and managing director: production planning, suppliers, commercial agreements, delivery. Now I turn operational problems into working tools with AI agents. My part is the one agents are worst at: deciding what "correct" means, and checking the result where it is actually used.

Spain · remote Europe / EMEA · Ukrainian, Russian, English

## Work you can check

Five cases in one shape: the problem, what I built or did, the number, and where to check it. Numbers carry the date they were measured.

**[ReadyCSV](https://www.readycsv.com)** · CSV preflight for HubSpot imports<br>
**Problem.** Agencies and RevOps consultants have to clean client CSVs before a HubSpot import, sometimes with data that may not leave their own environment.<br>
**Built.** A workspace that runs entirely in the browser: load a CSV, see blockers, warnings and safe fixes with the reason for each, repair in place, and export a cleaned copy with an issue report. No upload, no account, no AI calls.<br>
**Result.** Measured in release quality, not sales. In October a separate review reproduced a delimiter bug that made an uneven row look valid, and required a regression test before the fix shipped. The releases of 27 October and 2 November 2026 each passed 192 unit and 64 end-to-end tests before going live, then checks on the live site.<br>
**Check it.** [readycsv.com](https://www.readycsv.com), with a synthetic sample file. The code is private.

**[SkuSum](https://www.skusum.com)** · Amazon payouts into a journal that balances<br>
**Problem.** Amazon pays a seller one number per settlement, and the books need it split into a dozen categories that still tie back to that payout.<br>
**Built.** A web app and a Chrome extension that read the settlement report in the browser and produce a QuickBooks or Xero journal tied to the payout, plus profit per SKU when the orders, ads and cost files are added. No upload, no login, no Amazon connection. The journal balances in integer cents, and one that does not tie to the payout is not exported.<br>
**Result.** Accuracy was validated; willingness to pay was not. Across 8 genuine seller settlement files, all but 37 of 174,806 lines were placed automatically (census of 8 September 2026), and a draft from a real UK settlement imported into Xero as one valid journal that matches the payout (21 October). Suggestions from a public review thread became the export-blocking rule. On the market side, cold email to 165 bookkeeping firms brought one substantive reply, and the two bookkeepers who engaged in depth declined to pay: one needs a tool that fetches the data by itself, the other would not share client files. No paying customer as of 3 November 2026.<br>
**Check it.** [The web app](https://www.skusum.com/app/), the [Chrome Web Store listing](https://chromewebstore.google.com/detail/bjlbhfiacebdjjcblkhllhlobghakonp) and the [public review thread](https://www.indiehackers.com/post/built-a-local-first-amazon-profit-by-sku-quickbooks-xero-journal-tool-looking-for-founding-users-ce698322af). The code is private.

**Shared memory for AI agents** · the system behind [Agent Ops Notes](https://github.com/artemtrofymenko/agent-ops-notes)<br>
**Problem.** I build with four AI agents: Claude Code, Codex and two Hermes agents. Each session starts from zero, and each tool keeps its own notes, so two agents can give two different answers about what was decided.<br>
**Built.** One memory server that all four read and write through MCP. Before work an agent loads the project brief; after work it leaves a handoff that separates what was verified from what was not, with the changed files and the rollback. Curated records plus semantic search (Honcho, pgvector) on a VPS; a write that looks like a key or a config dump is rejected.<br>
**Result.** In the 7 days to 2 November 2026: 906 records from 4 agents across 27 projects, 488 of them handoffs.<br>
**Check it.** [Agent Ops Notes](https://github.com/artemtrofymenko/agent-ops-notes) describes the method and the incidents behind each rule. The memory itself is private.

**[career-ops](https://github.com/career-ops-hq/career-ops)** · open-source contributions<br>
**Problem.** An open-source AI job-search agent with over 79,000 stars had tests that were green on every CI platform and still failed, or never ran, on a default Windows install, and checks that could pass by looking in the wrong place.<br>
**Did.** Fixes, regression tests and reviews in a project I contribute to and did not create. Every change carries a number from before and after, and a new test shown failing against the old code.<br>
**Result.** [53 merged pull requests](https://github.com/career-ops-hq/career-ops/pulls?q=is%3Apr+author%3Aartemtrofymenko+is%3Amerged), 21 pull requests of other people reviewed and 15 issues filed, 12 of them closed, from 18 August to 3 November 2026. One of the latest: on a venture fund's job board the scanner read 18 listings and now reads 424 ([#6406](https://github.com/career-ops-hq/career-ops/pull/6406)). From the project author's [merge note](https://github.com/career-ops-hq/career-ops/pull/3267):

> Measured-not-reasoned on the actual machine it reproduces on is the gold standard.

**Check it.** [The full record](https://artemtrofymenko.github.io/open-source-record/), with each merged change up to 27 October, the maintainers' notes and what I could not verify.

**[LeakRelay](https://www.leakrelay.com/)** · missed-call response for restoration companies<br>
**Problem.** The idea: US water-damage restoration companies lose emergency jobs when nobody picks up after hours. Before building further, I needed to know whether that was true.<br>
**Did.** Paid for a mystery-call study: 20 companies in Dallas, Houston, Atlanta and Phoenix, called on weeknights after 7 pm with the same scenario, each call logged with its time and a screenshot. Then built a demo of the response: a missed call gets a text, and the owner gets a summary ready for the callback.<br>
**Result.** 5 of 20 answered with a live person and 8 through an answering service. 15 of 20 never called back within 24 hours; 2 sent a text. The gap was real, but cold outreach to about 8 marketing agencies and 15 owners produced no buyer conversation, and 8 of the 20 already relied on an answering service. I stopped the US push in July 2026 instead of sending another wave.<br>
**Check it.** [leakrelay.com](https://www.leakrelay.com/), with the demo video. The study data is private.

**[Agent Ops Notes](https://github.com/artemtrofymenko/agent-ops-notes)** · how I run AI agents<br>
Shared context, one writer per file, and checks made where the result lands rather than where the tool says it put it, with the incidents that taught me each rule.

Smaller: [Revenue Leak Roast](https://github.com/artemtrofymenko/RevenueLeakRoast), a deterministic offer teardown · [Telegram AI Automation Kit](https://github.com/artemtrofymenko/Telegram_AI_Automation_Kit_Public), a workflow UI with mock data.

## How I work

- Start from the operational decision, then pick the tool.
- Write down what "correct" means before anything is built.
- Check the output where it lands: the exported file, the live page, the record the next system reads.
- Every handoff says what was verified and what was not.

## Open to

Business Operations, AI workflow automation and internal tools roles, remote in Europe / EMEA.

**[LinkedIn](https://www.linkedin.com/in/trofymenko-artem/)** · **[GitHub](https://github.com/artemtrofymenko)**
