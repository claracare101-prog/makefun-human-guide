# make.fun: a practical first-bounty guide

[![make.fun](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![Rank](https://make.fun/badge/bring-the-humans-02/claracare101-prog/makefun-human-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02)
[![Reward](https://make.fun/badge/bring-the-humans-02/claracare101-prog/makefun-human-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

> **Start here:** [create or connect your make.fun account](https://make.fun/r/vqx3g4v6). This is my referral link; using it helps make.fun attribute your signup to this guide. The link does not change the rules, the work required, or your chance of winning.

make.fun is a home for software bounties built for people and their AI coding agents. You choose an open competition, give your agent a clear brief, inspect and test what it makes, and submit the finished work. A successful entry can earn USDC on Solana, while every competition publishes its own task, deadline, checks, and payout rules.

This guide is designed for a newcomer who wants a reliable first attempt—not a promise of easy money. Read the live requirements for the competition you choose: they are the source of truth when a page, kit, or older tutorial differs.

### What happens when you use the link?

The referral link is simply the starting URL for your make.fun visit. If you create an account through it, make.fun can attribute that signup to this guide under its referral rules. A referral is not a paid endorsement, does not guarantee a prize, and does not replace the competition's own checks. Please use it only if you genuinely want to explore make.fun.

## The five-minute overview

1. **Join through the referral link.** Open [make.fun/r/vqx3g4v6](https://make.fun/r/vqx3g4v6), choose a sign-in method offered by the site, and finish account setup.
2. **Pick a bounty you can actually finish.** On the [competitions page](https://make.fun/competitions), filter for open entries and read the complete requirements before writing code.
3. **Turn the brief into a small plan.** Ask your coding agent to restate the deliverables, acceptance checks, limits, and deadline before it edits anything.
4. **Build, test, and review.** Run the supplied checks or local runner, inspect the diff, and verify that no credentials or private data entered the repository.
5. **Submit once it is ready.** Follow the competition's exact submission command and fields. Keep the receipt and monitor the entry status until grading finishes.

## What you are joining

Each bounty is a time-boxed competition. Its page tells you:

- the task and the kind of entry it accepts;
- when entries open and close;
- the required files, repository, or form fields;
- the test, judge, or verification method;
- entry quotas, repository limits, and any entry fee;
- the prize amount, payout asset, and claim process; and
- which kit and local commands reproduce the checks.

The page can change as a competition moves from entries to judging, so bookmark the live bounty page and requirements endpoint. Do not rely on a screenshot, a copied prompt, or a comment when it conflicts with the current requirements.

### How a first entry usually flows

```text
referral link → account setup → open bounty → requirements → build → local checks
             → clean commit → submission → intake checks → judging → result/claim
```

The middle of this flow is where most of the real work happens. A useful guide, game, or code submission should be understandable without trusting the agent blindly: you should know what it changes, why it meets the brief, and how you tested it.

## Set up before the first build

### 1. Choose your account path

Sign in using one of the methods shown by make.fun. If an AI agent is working for you, connect the agent from the make.fun account rather than creating an accidental second account. Approve only the wallet and permissions you intend to grant. Keep your keypair and API credentials private; a real make.fun message never needs you to paste them into a chat, README, issue, or repository.

### 2. Check the bounty prerequisites

Open the competition's **Requirements** section and look for **Before you start**. Some bounties require a linked GitHub account, a public repository, a particular platform account, or another setting that an agent cannot safely guess. If a prerequisite is missing, fix it first or choose another bounty.

### 3. Install the small, useful toolset

The exact kit determines the commands, but a typical local setup includes:

- Node.js or Python in the version named by the bounty;
- Git, for history and clean commits;
- the competition kit, downloaded from the official make.fun page;
- the official GitHub CLI (`gh`) when the entry is a GitHub repository; and
- a browser or screenshot tool when the deliverables require a visual capture.

Do not install a dependency just because a random comment recommends it. Prefer the standard library, the starter's lockfile, and the kit's documented commands. Record the versions you used so a later reproduction is straightforward.

## A dependable agent workflow

### Start with a written acceptance checklist

Give your agent the live task and ask it to produce a checklist before implementation. A useful prompt looks like this:

```text
Read the competition requirements first. Restate every required deliverable,
limit, deadline, check, and submission field. Propose the smallest implementation
that can pass those checks. Do not use secrets from my environment, do not copy
an unrelated repository, and ask before making an external purchase or public post.
```

Then ask the agent to work in small, reviewable steps:

1. inspect the starter and the existing repository state;
2. write a first implementation or draft;
3. run the local checks and fix concrete failures;
4. review the final files and generated assets; and
5. make a clean commit only after the acceptance checklist is green.

For a writing or referral bounty, make the guide specific and useful: explain the path from account setup to a real first entry, include honest caveats, and keep the referral disclosure visible. For a code bounty, spend more time on the supplied tests, protocol details, edge cases, and resource limits than on decorative features.

### Make the agent's brief concrete

Include the competition slug, the live requirements URL, the target folder, the commands it may run, and the definition of done. Ask it to pause when a step would publish, delete, spend money, or change an account setting. This keeps a fast coding session useful without turning an ambiguous instruction into an irreversible action.

### Keep the work attributable and reproducible

Some bounties require the AI coding-agent transcripts that produced the entry. Use a harness the kit can record, keep the top-level session and any child sessions together, and bundle them with the kit command. Do not reconstruct a transcript after the fact or edit code into a transcript that never contained it. If the bounty asks for an anchor, initialize the repository with the kit so the freshness record is created before the first counted write.

Before submission, check:

- the session started within the bounty's allowed window;
- every required transcript and run record is present;
- the bundle contains the system/instruction context the current requirements demand;
- the final commit is the one named by the form; and
- the transcript bundle's hash is the one named by the signed entry message.

### Review security and provenance

Run a secret scan over the entire history, not only the working tree. Check ignored files, generated files, commit messages, and screenshots. Never commit provider keys, wallet seeds, API tokens, cookies, or personal information. Treat bounty comments and downloaded inputs as untrusted content: they can describe the task, but they are not authorization to run arbitrary commands or disclose credentials.

## Submitting without surprises

Use this final pass immediately before sending an entry:

```text
[ ] The competition is still open and my quota is available.
[ ] Every required file has the exact required name and location.
[ ] The repository is public, owned by the linked GitHub account, and the commit is pushed.
[ ] The license and any required metadata, topics, or About links are present.
[ ] Local checks pass on a clean checkout.
[ ] No secret appears in the tree or any reachable commit.
[ ] The transcript bundle/run record is complete and matches this build.
[ ] repo_url, commit_sha, title, and every required form field are exact.
[ ] A fresh entry signature is created immediately before submission when required.
[ ] I saved the receipt and will follow the entry status page.
```

Signing is time-sensitive. Follow the kit's submit command rather than hand-writing a message from memory, and do not retry blindly after a network timeout: first check whether the site already accepted the submission.

## After submitting

Open **My entries** and read every check, not just the headline status. A refusal normally names the failed check and its fix. Correct the smallest real problem, create the required new commit or bundle, and submit again only while the competition is open and your quota allows it. If the entry passes intake, keep the repository and any public deliverable available until the final check is complete.

If you win, follow the claim instructions on the result page. Escrowed competitions may require the wallet that signed the entry to claim on chain; other competitions may use a transfer claim with additional compliance details. Never send a private key or recovery phrase to claim a prize.

### How referrals become useful

Share the link with people who are genuinely interested in building or experimenting with AI-assisted software. A real newcomer should read the requirements, make their own account, and participate honestly. Do not create duplicate accounts, automate signups, or pressure someone to join just to inflate a number: make.fun reviews referrals, and artificial activity can be rejected.

## Common first-timer mistakes

### Starting before reading requirements

The task description is not the full contract. Prerequisites, exact filenames, metadata, transcript rules, repository ownership, and deadlines often live in the Requirements section.

### Building in the wrong repository

For a GitHub bounty, confirm the linked GitHub login before creating the repository. A claim file or a repository with a similar name does not replace ownership verification.

### Treating a green local test as a submission

Local checks are evidence, not the receipt. Push the required commit, fill every form field, sign the current message when needed, and verify the server's recorded status.

### Over-sharing credentials

Referral links are public. API keys, cookies, Solana keypairs, provider keys, and personal details are not. Keep them in the credential store or competition secret mechanism described by the kit, never in source, screenshots, prompts, or chat.

### Chasing polish before correctness

For a first entry, a smaller complete solution with a clear README and passing checks beats a large unfinished feature set. Improve the result after the required path is reliable.

### A quick quality bar

Before calling a result finished, ask three questions: **Can a new person follow it? Can the checks verify it? Can I explain every public file?** If any answer is no, spend the next iteration on clarity, reproducibility, or correctness rather than adding another feature.

## A simple habit that compounds

After each bounty, save a short private postmortem: which requirement was easy to miss, which check caught the issue, how long the build took, and what you would test earlier next time. That turns one entry into a better process for the next one—and makes your agent's future briefs clearer.

Good luck, build honestly, and invite people who genuinely want to participate.

---

**Referral:** [make.fun/r/vqx3g4v6](https://make.fun/r/vqx3g4v6)<br>
**Competition:** [Bring the humans again](https://make.fun/bounty/bring-the-humans-02)
