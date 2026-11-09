> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · This page does not start a machine.

# Plan

The day is **Wed 11 Nov 2026**. T0 is 12:00 UTC. The repo is `tn10-storm-2026-11-11`. The standing rule is [RULES.md](../RULES.md). The pastes carry this clock. They refuse to start until `REVIEW_CLOSED` is in [prompts/REVIEW.md](../prompts/REVIEW.md). This clock is try 1. The reasoning is [TRIES.md](TRIES.md).

## Families

Sixteen covenant families, all on from T0 until recovery ends. Offer **1.2 hop/s per family**. Boson. Stagger 0. No phase offset. One desk sender for the families. One genesis.

The quiet goal is one 900-second window in which every family has at least **1,026** accepted hops. When that window closes, the payment climb begins at the next minute. If 13:00 UTC arrives first, the runner writes `QUIET_MISS` and begins the climb. One quiet phase. It is not repeated.

## Payment offers

The capacity line is **3,040** simple payments per second. The offers are one third, two thirds, three thirds, and four thirds of that line. The desk sends the whole offer. One machine.

| Step | Offer, tx/s | Desk |
|---:|---:|---:|
| 1 | 1,013 | 1,013 |
| 2 | 2,027 | 2,027 |
| 3 | 3,040 | 3,040 |
| 4 | 4,053 | 4,053 |

The 6–7 Oct desk hold of 2,207 tx/s was with a local node also verifying. Offering 4,053 from this machine, with that process stopped, has not been measured. If a step is not stable, the phase file says `SHORT` and the climb stops. The next phase is the step-down.

## Stable, then thirty minutes

A step is stable when three consecutive full minutes all have:

- Mini's node synced, and the DAA moving
- the public submit path answering
- no sender-off, pool-low, node-drop, or proc-exit
- at least 8 merged blocks per second on Mini's read
- the payment offer within 10 percent of that step's number

The thirty minutes start on the next minute. They are not restarted because one minute inside them dips. Three consecutive minutes that break the list end the hold. The file keeps the minutes already counted. The climb stops. The step-down begins.

The approach may take up to 20 minutes. If the step is not stable by then, the file says `SHORT` and the climb stops.

## Latest minute

A phase that would start after its latest minute is skipped. The runner writes the SKIP file and goes to the step-down, then recovery. Recovery still starts by 16:30 UTC. If the path is already inside recovery at 16:30, it continues. Recovery runs two hours, and it ends by 18:30 UTC.

| Phase | Latest start, UTC |
|---|---|
| Quiet | 12:00, fixed |
| Hold 1, including its approach | 13:00 |
| Hold 2 | 13:50 |
| Hold 3 | 14:40 |
| Hold 4 | 15:30 |
| Step-down | 16:20 |
| Recovery | 16:30 |

## Step-down and recovery

From whatever offer is live, the payment offer steps to the next lower line every two minutes until it is 1,013 tx/s. That step-down is at most 10 minutes. Then the families and the 1,013 tx/s payment offer run together for two hours.

## Fees

Fixed for the whole clock. Minimum relay is 100 sompi per gram. Families 1–13 pay 100. Families 14–16 pay 200. Every payment sender pays 150. A submit rejected for the fee stops that sender. The rate is not raised. A node's priority quote is not read.

## Funding

Recount before the 11:50 genesis. The abort line stays **2,500 coins** and **18,000 usable tKAS**. Do not lower it. Do not spend a mining coin at or above 100,000 tKAS. Do not print a balance, a key, or an id. One coin per family for the one genesis. The same lineage runs all day.

## Abort

Stop the affected sender on sender-off, pool-low, node-drop, or proc-exit. A submit path that is not synced does not get a start. A failed submit is a reject.

Tuesday's runner uses the desk node. This neuron leaves that process up until Tuesday's runner is down. Before Wednesday genesis the desk stops its node process. The chain data stays on disk. The senders submit to public TN10 nodes. The process stays stopped until the method file is on origin. Then it may be started again. The data is not deleted. The binary is not switched. An index is not turned on.

Miners stay off. A stretch under 8 merged blocks per second is recorded as miner-out. It is not scored as a family failure, and it is not a stable minute.

## What this plan does not change

Tuesday's repo, the 8 Nov rehearsal, and the 8 Nov confirmation stay on their clocks. 43b is [LATER.md](LATER.md).
