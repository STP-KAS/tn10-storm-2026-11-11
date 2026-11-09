> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · This page does not start a machine.

# Plan

The day is **Wed 11 Nov 2026**. T0 is 12:00 UTC. The repo is `tn10-storm-2026-11-11`. The standing rule is [RULES.md](../RULES.md). The pastes carry this clock. They refuse to start until `REVIEW_CLOSED` is in [prompts/REVIEW.md](../prompts/REVIEW.md). This clock is try 1. The reasoning is [TRIES.md](TRIES.md).

## Families

Sixteen covenant families, all on from T0 until the last payment target is met. Offer **1.2 hop/s per family**. Boson. Stagger 0. No phase offset. One desk sender for the families. One genesis.

**1,026** accepted hops per family in one 900-second window is a score inside the files. It does not open a payment target and it does not close one. The 1.2 offer stays.

## Payment targets

The capacity line is **3,040** simple payments per second. The desk sends the whole offer. One machine. The targets are in this order. The next offer starts when the current target is met.

| Order | Offer, tx/s | File |
|---:|---:|---|
| 1 | 1,013 | HOLD-1 |
| 2 | 2,027 | HOLD-2 |
| 3 | 3,040 | HOLD-3 |
| 4 | 4,053 | HOLD-4 |
| 5 | 1,013 | RETURN |

The 6–7 Oct desk hold of 2,207 tx/s was with a local node also verifying. Offering 4,053 from this machine, with that process stopped, has not been measured. A miss stays on that offer.

## When a target is met

A target is met when three consecutive full minutes all have:

- Mini's node synced, and the DAA moving
- the public submit path answering
- no sender-off, pool-low, node-drop, or proc-exit
- at least 8 merged blocks per second on Mini's read
- the payment offer within 10 percent of that target's number
- every family still attempting hops

The run has a start. It has no latest minute. A missed minute does not skip the target and does not pick a new T0. The same offer stays until the three clean minutes land. Then the file is published and the next offer starts.

Each miss is a line in [logs/FIXES.md](../logs/README.md): the UTC time, what failed, what was changed, and why that change. The fee stays. The offer number stays until the target is met. The plan pages stay as they were at 11:20 UTC.

A repair may restart the sender, move the submit to another public TN10 node, or repair the builder. A repair does not raise the fee, start the desk node, switch the binary, turn on an index, bring the bot in, or open a second runner. When none of those repairs can make the minute clean, the run stops and the method file is written. The abort line is not lowered to keep the offer alive.

When RETURN is met, the families stop and the payments stop.

## Fees

Fixed for the whole run. Minimum relay is 100 sompi per gram. Families 1–13 pay 100. Families 14–16 pay 200. Every payment sender pays 150. A submit rejected for the fee stops that sender. The rate is not raised. The miss is a line in the fix log, and the same offer resumes when that sender can submit at the same fee. A node's priority quote is not read.

## Funding

Recount before the 11:50 genesis. The abort line stays **2,500 coins** and **18,000 usable tKAS**. Do not lower it. Do not spend a mining coin at or above 100,000 tKAS. Do not print a balance, a key, or an id. One coin per family for the one genesis. The same lineage runs all day. Each landed hop locks about 1 tKAS. A target with no end time can use more of the lane than a timed hold. The abort line still stops the sender.

## Abort

A sender-off, pool-low, node-drop, or proc-exit stops that sender. The line goes into the fix log. The same target resumes when the abort line is true again and the submit path answers. A submit path that is not synced does not get a start. A failed submit is a reject.

Tuesday's runner uses the desk node. This neuron leaves that process up until Tuesday's runner is down. Before Wednesday genesis the desk stops its node process. The chain data stays on disk. The senders submit to public TN10 nodes. The process stays stopped until the method file is on origin. Then it may be started again. The data is not deleted. The binary is not switched. An index is not turned on.

Miners stay off. A stretch under 8 merged blocks per second is recorded as miner-out. It is not scored as a family failure, and it is not a stable minute.

## What this plan does not change

Tuesday's repo, the 8 Nov rehearsal, and the 8 Nov confirmation stay on their clocks. 43b is [LATER.md](LATER.md).
