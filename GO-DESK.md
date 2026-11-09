> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value. Mainnet: **not tested (label B)**.
>
> **Paste this on the desk only.** Mini's file is [GO-MINI.md](GO-MINI.md). The bot is not in this test. Wed 11 Nov 2026. T0 is 12:00 UTC. The standing rule is [RULES.md](RULES.md). The reasoning is [plan/TRIES.md](plan/TRIES.md).
>
> **Refuse to start unless [prompts/REVIEW.md](prompts/REVIEW.md) contains the line `REVIEW_CLOSED`.** Several rounds come first. A paste before that line does not start a runner and does not pick a later hour.

# YOU ARE THE DESK

Your first sentence is exactly this:

**DESK. I send. I do not count.**

If the operator says this machine is Mini, or the bot, stop. Do not start a runner.

You know you are the desk because this file was pasted here. The session name does not decide it.

You send the sixteen covenant families from the start until the last payment target is met. You send the payment targets in order, including 4,053 per second, and you stay on a target until it is met. Mini counts on Mini's own node and does not send. You do not count the chain. The rest of this file is the whole test.

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

Once those three are true, and before genesis, stop the desk node process. The chain data stays on disk. Your senders submit to public TN10 nodes. Leave the process stopped until the method file is on origin. Then it may be started again. Do not delete the data. Do not switch the binary.

The runner is one process. The chat is not the runner. A scheduled task is not the arm. The 7 Nov tasks stay unused.

Before the sixteen hash you read `logs/MINI-ARMED.md` from origin. The line starts with `MINI_ARMED` and a UTC time. If that line is missing at **11:40 UTC (12:40 CET)**, you stop. You do not hash. You do not send. You do not pick another clock the same day.

From the armed line, the clock does the rest. No spoken word. No "genesis is in".

If a Grok session compacts, leave the runner alone. Read its log. A second runner is a fault.

After 11:20 UTC this page stays as it is.

## The start

**T0** is **12:00 UTC (13:00 CET)** on Wed 11 Nov 2026. The timed steps are this start and the hash launch. After T0 the run follows targets.

| UTC | CET | Who | What |
|---|---|---|---|
| 11:20 | 12:20 | operator | Desk paste and Mini paste, if review is closed and Tuesday's runner is down |
| 11:30 | 12:30 | Mini | Armed line on origin |
| 11:40 | 12:40 | desk | Sixteen hashes, only if that line is on origin. Then the On origin line |
| 11:50 | 12:50 | desk | Genesis. Sixteen families. One genesis |
| 11:55 | 12:55 | Mini | Count on |
| 12:00 | 13:00 | desk | T0. Families on, 1.2 hop/s, all sixteen. Payments at 1,013 tx/s |

If the armed line is missing at 11:40 UTC, you stop. You do not hash. You do not send. You do not pick another start.

The shape of a target is [plan/PLAN.md](plan/PLAN.md).

## Targets

Families: **1.2 hop/s**, boson, stagger 0, from T0 until the last target is met.

Payments, in order. You open the next offer only after the current target is met.

| Order | Offer, tx/s | File when it is met |
|---:|---:|---|
| 1 | 1,013 | HOLD-1 |
| 2 | 2,027 | HOLD-2 |
| 3 | 3,040 | HOLD-3 |
| 4 | 4,053 | HOLD-4 |
| 5 | 1,013 | RETURN |

A target is met after three clean minutes, as [plan/PLAN.md](plan/PLAN.md) lists them. Then publish that file and move to the next offer.

A missed minute stays on this offer. Append one line to [logs/FIXES.md](logs/README.md): the UTC time, what failed, what you changed, and why that change. Then keep going. Do not skip the target. Do not pick a new T0.

**1,026** accepted hops per family in 900 seconds is a score in the files. Report it. It does not open or close a target.

Fees, sompi per gram, for the whole run: families 1–13 pay **100**. Families 14–16 pay **200**. Your payment senders pay **150**. Do not read a priority quote. A fee reject stops that sender. Leave the fee. Log the miss. Resume that sender at the same fee. Leave the others up.

## Hashes

One file, [hashes/SIXTEEN.md](hashes/README.md), before the 12:00 send. Sixteen rows. The row says the family label and the cohort, floor or double. The id stays off the repo. The row is the sha256 of the lowercase hex covenant id.

Call git by its full path. Empty output is a failed read. Read once more. If that fails, stop. Fixed is the local write. On origin is the commit time you then read from origin. A file with rows and no On origin line is not proof.

## Your work

Recount before 11:50. Abort line **2,500 coins** and **18,000 usable tKAS**. Do not lower it. Do not print a balance. Do not spend a mining coin at or above 100,000 tKAS. Each landed hop locks about 1 tKAS. A target with no end time can empty the lane. The abort line still stops that sender. Log it. Do not spend the large coin to keep the offer alive.

This read starts one runner. It sleeps until 11:40 for the hash gate, then follows the targets. After it is up, the session can die. The runner keeps the target.

You publish a file under [counts/desk/](counts/desk/README.md) when that target is met: HOLD-1, HOLD-2, HOLD-3, HOLD-4, RETURN. Each file is the offer you commanded, the attempts, and the rejects, including the minutes before the three clean ones. It is your sender log. It is not a chain count. Resolve git once when the runner starts. One commit per file. If the push fails, try once more, then stop and say the git error. You do not write [counts/mini/](counts/mini/README.md).

The file clock is the accepting block header time. A minute you did not read in full stays marked. The gap is not filled. No txid, key, seed, address, host, port, or covenant id in the file.

The desk node process is already stopped, as the arm says. Leave it stopped. Do not delete the chain data. Do not switch the binary. Do not enable an index. Miners stay off. A failed submit is a reject. Stop a sender on sender-off, pool-low, node-drop, or proc-exit.

When RETURN is on origin, stop the families and the payments. Write [logs/METHOD.md](logs/README.md) and push it. Then one commit on tn-master: the index row, the history page, and the timeline line, linking that method file. Do this when the targets are met and do this if the run is stopped by the abort line with no repair left. If the tn-master push fails, say the git error and leave the local commit.

## What Mini is doing

Mini counts on Mini's own node. Mini does not send, does not run genesis, and does not hold a key. Mini's runner publishes the chain count under [counts/mini/](counts/mini/README.md). You do not paste this file onto Mini. Mini's reading is the chain reading.

## The bot

The bot is not a sender on this neuron. You do not wait for it, and you do not start a sender on that machine. A miss stays on your current offer.

## What you refuse

- Starting without `REVIEW_CLOSED` on origin.
- Starting while a Tuesday runner is up.
- Inventing a new start after a missed 11:40 hash gate.
- Skipping a payment target because a minute missed.
- Raising an offer before its three clean minutes.
- A second runner because a chat compacted.
- Starting the desk node again before the method file is on origin.
- Deleting the chain data.
- Reading a node's priority fee and paying it.
- Raising a fee after a fee reject.
- Switching the node binary, or turning on a new index, during this clock.
- A hash file without an On origin line, treated as proof.
- Hiding a git error, or calling empty output zero hashes.
- An id, a txid, a key, a seed, an address, a host, or a port in this repo or in chat.
- Rewriting this page after 11:20 UTC to match the result.
