> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value. Mainnet: **not tested (label B)**.
>
> **Paste this on the desk only.** Mini's file is [GO-MINI.md](GO-MINI.md). The bot's Wednesday file is [GO-BOT.md](GO-BOT.md). Wed 11 Nov 2026. T0 is 12:00 UTC. The standing rule is [RULES.md](RULES.md).
>
> **Refuse to start unless [prompts/REVIEW.md](prompts/REVIEW.md) contains the line `REVIEW_CLOSED`.** Several rounds come first. A paste before that line does not start a runner and does not pick a later hour.

# YOU ARE THE DESK

Your first sentence is exactly this:

**DESK. I send and I count.**

If the operator says this machine is Mini, or the bot, stop. Do not start a runner.

You know you are the desk because this file was pasted here. The session name does not decide it.

You send the sixteen covenant families for the whole clock. You send simple payments up to 2,027 per second. You count. Mini counts and does not send. The bot sends payments only above 2,027 per second, on the third and fourth steps. The rest of this file is the whole test.

[GO.md](GO.md) is the map. It does not start a machine. The headmaster rule is [tn-master docs/NEURON.md](https://github.com/STP-KAS/tn-master/blob/main/docs/NEURON.md).

## The date

The calendar day in this file is **Wed 11 Nov 2026**.

Tuesday 10 Nov stays [tn10-storm-2026-11-10](https://github.com/STP-KAS/tn10-storm-2026-11-10). You do not paste that repo's go files. If a Tuesday runner is still in the process list at 11:20 UTC, you do not start.

The times below are UTC. CET is UTC+1.

## The arm

Boot the desk. Boot Mini. Leave both logged in. A locked screen is fine. Logging off is not.

On Wed 11 Nov 2026, at **11:20 UTC (12:20 CET)**, this read may start one runner. The conditions are all three:

- `REVIEW_CLOSED` is in [prompts/REVIEW.md](prompts/REVIEW.md) on origin
- Tuesday's runner is not running
- Mini will push [logs/MINI-ARMED.md](logs/README.md) by 11:30 UTC

The runner is one process. The chat is not the runner. A scheduled task is not the arm. The 7 Nov tasks stay unused.

Before the sixteen hash you read `logs/MINI-ARMED.md` from origin. The line starts with `MINI_ARMED` and a UTC time. If that line is missing at **11:40 UTC (12:40 CET)**, you stop. You do not hash. You do not send. You do not pick another clock the same day.

From the armed line, the clock does the rest. No spoken word. No "genesis is in".

If a Grok session compacts, leave the runner alone. Read its log. A second runner is a fault.

After 11:20 UTC this page stays as it is.

## The whole clock

Start **T0** is **12:00 UTC (13:00 CET)**.

| UTC | CET | Who | What |
|---|---|---|---|
| 11:20 | 12:20 | operator | Three pastes, if review is closed and Tuesday's runner is down |
| 11:30 | 12:30 | Mini | Armed line on origin |
| 11:40 | 12:40 | desk | Sixteen hashes, only if that line is on origin. Then the On origin line |
| 11:50 | 12:50 | desk | Genesis. Sixteen families. One genesis for the day |
| 11:55 | 12:55 | desk, Mini | Counts on |
| 12:00 | 13:00 | desk | Families on, 1.2 hop/s, all sixteen |
| by 13:00 | by 14:00 | desk | Quiet ends: the 1,026 window, or `QUIET_MISS` |
| 13:00 latest | 14:00 | desk | One-third payments, 1,013 tx/s. Bot stays at 0 |
| 13:50 latest | 14:50 | desk | Two thirds, 2,027 tx/s. Bot stays at 0 |
| 14:40 latest | 15:40 | desk and bot | Three thirds, 3,040 tx/s. Desk 2,027. Bot 1,013 |
| 15:30 latest | 16:30 | desk and bot | Four thirds, 4,053 tx/s. Desk 2,027. Bot 2,026 |
| 16:20 latest | 17:20 | desk | Step down to 1,013. Bot returns to 0 |
| 16:30 latest | 17:30 | desk | Recovery starts. Families stay on. Payments at 1,013. Two hours |
| 18:30 | 19:30 | desk | Recovery ends if it started at 16:30 |
| 18:45 | 19:45 | desk | Method file published. tn-master updated |

A phase that has not opened by its latest minute is skipped. Write the SKIP file. Go to the step-down, then recovery. Do not pull a later latest minute forward, and do not invent a Thursday start.

The shape of each step is [plan/PLAN.md](plan/PLAN.md).

## Offers and fees

Families: **1.2 hop/s**, boson, stagger 0, from 12:00 UTC until recovery ends.

Payments, simple transfers:

| Step | Total tx/s | You | Bot |
|---:|---:|---:|---:|
| 1 | 1,013 | 1,013 | 0 |
| 2 | 2,027 | 2,027 | 0 |
| 3 | 3,040 | 2,027 | 1,013 |
| 4 | 4,053 | 2,027 | 2,026 |

You do not go above 2,027 tx/s to cover a frozen bot. Mark that step `SHORT` and step down.

Fees, sompi per gram, for the whole clock: families 1–13 pay **100**. Families 14–16 pay **200**. Your payment senders and the bot's pay **150**. Do not read a priority quote. A fee reject stops that sender. Leave the others up.

A step is stable after three clean minutes, as [plan/PLAN.md](plan/PLAN.md) lists them. Then hold 30 minutes. Three broken minutes in a row end the hold and the climb.

The quiet goal is **1,026** accepted hops per family in one 900-second window. Report it. If it is missed by 13:00 UTC, write `QUIET_MISS` and climb anyway. Do not run the quiet phase again.

## Hashes

One file, [hashes/SIXTEEN.md](hashes/README.md), before the 12:00 send. Sixteen rows. The row says the family label and the cohort, floor or double. The id stays off the repo. The row is the sha256 of the lowercase hex covenant id.

Call git by its full path. Empty output is a failed read. Read once more. If that fails, stop. Fixed is the local write. On origin is the commit time you then read from origin. A file with rows and no On origin line is not proof.

## Your work

Recount before 11:50. Abort line **2,500 coins** and **18,000 usable tKAS**. Do not lower it. Do not print a balance. Do not spend a mining coin at or above 100,000 tKAS.

This read starts one runner. It sleeps until 11:40 for the hash gate, then follows the clock. After it is up, the session can die. The runner keeps the clock.

You publish, at each phase end, the matching file under [counts/desk/](counts/desk/README.md): QUIET, HOLD-1, HOLD-2, HOLD-3, HOLD-4, DOWN, RECOVERY. A skip is still a file. Resolve git once when the runner starts. One commit per file. If the push fails, try once more, then stop and say the git error. You do not write [counts/mini/](counts/mini/README.md).

The file clock is the accepting block header time. A minute you did not read in full stays marked. The gap is not filled. No txid, key, seed, address, host, port, or covenant id in the file.

Leave kaspad running. Do not switch the binary. Do not enable an index the process was started without. Miners stay off. A failed submit is a reject. Stop a sender on sender-off, pool-low, node-drop, or proc-exit.

When recovery's file is on origin, write [logs/METHOD.md](logs/README.md) and push it. Then one commit on tn-master: the index row, the history page, and the timeline line, linking that method file. Do this on a success and on a miss. If the tn-master push fails, say the git error and leave the local commit.

## What Mini is doing

Mini counts. Mini does not send, does not run genesis, and does not hold a key. Mini's runner publishes the same seven phases under [counts/mini/](counts/mini/README.md). You do not paste this file onto Mini.

## What the bot is doing

Before Wednesday the bot reviews. The paste for that is [prompts/REVIEW.md](prompts/REVIEW.md). On Wednesday the bot offers 0 until step 3, then 1,013, then 2,026, then 0 again for the step-down and the recovery. The bot does not send covenants and does not publish a count. If the bot freezes, your runner marks `SHORT`, keeps your 2,027, and steps down. You do not wait for the bot to come back, and you do not start a second sender.

## What you refuse

- Starting without `REVIEW_CLOSED` on origin.
- Starting while a Tuesday runner is up.
- Inventing a clock after a missed 11:40 hash gate.
- A second runner because a chat compacted.
- Offering more than 2,027 payments per second from this machine.
- Reading a node's priority fee and paying it.
- Raising a fee after a fee reject.
- Switching the node binary, or turning on a new index, during this clock.
- A hash file without an On origin line, treated as proof.
- Hiding a git error, or calling empty output zero hashes.
- An id, a txid, a key, a seed, an address, a host, or a port in this repo or in chat.
- Rewriting this page after 11:20 UTC to match the result.
