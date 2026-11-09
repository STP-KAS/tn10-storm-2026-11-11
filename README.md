> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value. **Wed 11 Nov 2026, 12:00 UTC (13:00 CET).** Mainnet: **not tested (label B)**.
>
> **Not armed.** [prompts/REVIEW.md](prompts/REVIEW.md) does not yet contain `REVIEW_CLOSED`. A read does not start a runner. This clock is try 1. The reasoning is [plan/TRIES.md](plan/TRIES.md). The operator writes the closed line. Then, on Wednesday, the operator sends the desk paste and the Mini paste.
>
> **Part of [tn-master](https://github.com/STP-KAS/tn-master)**, the map of every TN10 storm. The rule for every neuron is [docs/NEURON.md](https://github.com/STP-KAS/tn-master/blob/main/docs/NEURON.md).

# tn10-storm-2026-11-11

**History of every storm: [MASTER.md](https://github.com/STP-KAS/tn-master/blob/main/history/MASTER.md)** (in tn-master).

**Tuesday stays Tuesday:** [tn10-storm-2026-11-10](https://github.com/STP-KAS/tn10-storm-2026-11-10), T0 19:00 UTC on 10 Nov 2026. This repo does not move that clock. File 1 of that count is due here on Wednesday at 12:00 CET (11:00 UTC), in that repo.

**The form this plan copies:** [tn10-storm-2026-11-08-confirm](https://github.com/STP-KAS/tn10-storm-2026-11-08-confirm). That night finished at 16:10 UTC. Both publishers fired. The reading is [logs/METHOD.md](https://github.com/STP-KAS/tn10-storm-2026-11-08-confirm/blob/main/logs/METHOD.md).

## The pastes

One story. One file for each computer. Paste the file that names the machine in front of you. The first sentence must be that machine. If it names another one, stop and paste the other file.

| Machine | Paste | First sentence | When |
|---|---|---|---|
| **bot, for the review** | [prompts/REVIEW.md](prompts/REVIEW.md) | GROKBOT. I review. I do not send. | before Wednesday, and not during Tuesday's window |
| **desk** | [GO-DESK.md](GO-DESK.md) | DESK. I send. I do not count. | Wed 11 Nov, 11:20 UTC, after `REVIEW_CLOSED` |
| **Mini** | [GO-MINI.md](GO-MINI.md) | MINI. I count. I do not send. | the same minute |

Each go file is the whole plan. Grok Build does not guess the machine from its own name. The pasted file is the machine. [GO.md](GO.md) is the map. It does not start a session.

The operator writes `REVIEW_CLOSED` when this shape is the one he wants. The bot does not write that line. A Wednesday paste before that line refuses to start, and it does not pick a later hour. The bot is not a sender. [GO-BOT.md](GO-BOT.md) refuses to start one.

## Clock

Times are UTC first. Desk local is CET (UTC+1). The timed steps are the start and the hash launch. After T0 the run follows targets. It stays on a target until that target is met.

| | UTC | CET |
|---|---|---|
| Tuesday's File 1 is due, in the Tuesday repo | 11:00 | 12:00 |
| Operator sends the desk paste and the Mini paste, if review is closed and Tuesday's runner is down | **11:20** | **12:20** |
| Mini's armed line on origin | **11:30** | **12:30** |
| Sixteen hashes proved, or the desk stops | **11:40** | **12:40** |
| Genesis | 11:50 | 12:50 |
| Mini's count on | 11:55 | 12:55 |
| **START (T0).** Families on. Payments at one third | **12:00** | **13:00** |

The targets are one third, two thirds, three thirds, four thirds, then one third again. They are in [plan/PLAN.md](plan/PLAN.md). The same start is in the desk paste and the Mini paste. There is no latest minute after T0.

## What and why

**What.** Sixteen covenant families, on from T0 until the last payment target is met. Offer 1.2 hop/s per family. Boson. Stagger 0. Families 1–13 pay 100 sompi/gram. Families 14–16 pay 200. Payment senders pay 150. The payment targets are 1,013 tx/s, then 2,027, then 3,040, then 4,053, then 1,013 again. The desk sends all of it and stays on a target until three clean minutes land. A miss is logged and repaired on that same offer. Mini is the only chain counter. The desk node process is stopped for the send, after Tuesday's runner is down, and the senders use public TN10 nodes. The chain data stays. The bot stays out. Miners stay off.

**Why.** The full why is [WHY.md](WHY.md). The mass-ceiling line used here is 3,040 payments per second. Sixteen is the largest mix whose confirm reading cleared 1,026 hops per family in 900 seconds.

## Review

The bot stays out of this test. Its machine freezes. [GO-BOT.md](GO-BOT.md) does not start a sender. A review file, if one is still wanted on another day, is [prompts/REVIEW.md](prompts/REVIEW.md). Do not paste it during Tuesday 18:20–22:15 UTC. A review round is a file in this repo. It is not a load.

## Map

| Path | What is in it |
|---|---|
| [BENCHMARK.md](BENCHMARK.md) | What this plan copies from the confirmation |
| [DISCLAIMER.md](DISCLAIMER.md) | Experimental. Certainty labels A / B / C |
| [WHY.md](WHY.md) | Why this clock, and the lines it uses |
| [RULES.md](RULES.md) | Who publishes, how a hash file is proved, one runner |
| [GO.md](GO.md) | Map of the pastes. Does not start a machine |
| [GO-DESK.md](GO-DESK.md) | Desk paste |
| [GO-MINI.md](GO-MINI.md) | Mini paste |
| [GO-BOT.md](GO-BOT.md) | Bot paste. It refuses to send |
| [plan/TRIES.md](plan/TRIES.md) | Why try 1 is shaped this way, and why more runs are expected |
| [prompts/REVIEW.md](prompts/REVIEW.md) | Bot paste for the review. This is the one to send first |
| [go/README.md](go/README.md) | Which paste goes on which computer |
| [plan/PLAN.md](plan/PLAN.md) | Offers, fees, and when a target is met |
| [plan/COUNT.md](plan/COUNT.md) | How a hop and a payment are counted |
| [plan/LATER.md](plan/LATER.md) | What was left off this clock |
| [hashes/README.md](hashes/README.md) | One hash file. Absent until the desk runner writes it |
| [counts/desk/README.md](counts/desk/README.md) | The desk's phase files |
| [counts/mini/README.md](counts/mini/README.md) | Mini's phase files |
| [logs/README.md](logs/README.md) | The armed line, the fix log, and the method file |

Counts only. No key, seed, txid, covenant id, address, host or port in this repo.
