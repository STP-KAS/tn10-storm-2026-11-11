> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · This page does not start a machine.

# Plan

The day is **Wed 11 Nov 2026**. T0 is 12:00 UTC. The repo is `tn10-storm-2026-11-11`. The standing rule is [RULES.md](../RULES.md). The pastes carry this clock. They refuse to start until `REVIEW_CLOSED` is in [prompts/REVIEW.md](../prompts/REVIEW.md). This clock is try 1. The reasoning is [TRIES.md](TRIES.md).

## Families

Sixteen covenant families, all on from T0 until the last payment target is met. Offer **1.2 hop/s per family**. Boson. Stagger 0. No phase offset. One desk sender for the families. One genesis.

**1,026** accepted hops per family in one 900-second window is a score inside the files. It does not open a payment target and it does not close one. The 1.2 offer stays.

## Payment targets

The capacity line is **3,040** simple payments per second. Finding 1 puts the band at 3,040 to 3,080. Submitting faster fills mempools. HOLD-1, HOLD-2, HOLD-3, and RETURN are scored. The desk sends those alone. HOLD-4 is an observation. It is not scored.

| Order | Offer, tx/s | Who sends | File | Kind |
|---:|---:|---|---|---|
| 1 | 1,013 | desk | HOLD-1 | scored |
| 2 | 2,027 | desk | HOLD-2 | scored |
| 3 | 3,040 | desk | HOLD-3 | scored |
| 4 | 4,053 | desk, and the bot if a free synced node answers | HOLD-4 | observation |
| 5 | 1,013 | desk | RETURN | scored |

The 6–7 Oct hold of 2,207 tx/s seen accepted was twelve signers on public nodes. The desk node was still syncing and took no traffic. The highest sustained submit on that page is 2,210 over six public nodes. HOLD-3 needs at least 2,736 submit-OK per second. That is above the sustained record. HOLD-3 is the expected first miss. A miss is published. The offer is not lowered to hide it.

Payment senders spread across every public node that answers synced. One process per node. A node that does not answer is skipped. Two processes do not share one node. The node list stays off this repo. The desk keeps that set through HOLD-4. It does not drop a node to free one for the bot. Families 1–13 and families 14–16 use the same family-sender nodes. A repair that moves the family sender moves both cohorts.

Before the 11:40 hash the desk checks each public node in the local config. The check is version, synced, DAA within a few blocks of the others, UTXO index, and answer time. A node that fails is dropped before the hash. It is not put back after T0. The local log keeps the count of nodes checked and pass or fail. No names. The 6 Oct per-node hold is about 571 seen accepted. If the kept nodes times 571 sit under 1,824, the local log says HOLD-2 is the expected first miss. The offers stay. This page keeps HOLD-3 as the expected first miss, from the six-node record of 2,210.

## When a scored target is met

A scored target is met when three consecutive full minutes all have:

- the desk's read of its submit path: that node's own synced flag is true, and that node's DAA score is moving. This is the desk's read. It is not a chain count
- submit-OK within 10 percent of that target's number
- rejects logged, split into rate and full
- no sender-off, pool-low, node-drop, or proc-exit
- every family still attempting hops

Mini's file sits beside the desk file. Mini's non-coinbase count includes base load. The two readings are not averaged. Mini's sync, Mini's DAA, and merged blocks per second are marks in Mini's file. They do not gate the next offer. Mempool size, free memory, and CPU stay in Mini's local log. If a read is slow, or memory runs short, those three go first. The hop count stays.

The run has a start. It has no latest minute. A missed minute stays on that offer. It does not pick a new T0. Each miss is a line in [logs/FIXES.md](../logs/README.md): the UTC time, what failed, what was changed, and why that change. The fee stays. The plan pages stay as they were at 11:20 UTC.

A repair may restart the sender, move the submit to another public node that answers synced, or repair the builder. Each of those is tried once for that reason and logged. Waiting for the same reject to clear is not another try. A new reason gets its own pass.

A repair does not raise the fee, start the desk node, switch the binary, turn on an index, bring the bot in, or open a second runner. That bot line holds for HOLD-1, HOLD-2, HOLD-3, and RETURN.

When the pass is done and the minute is still dirty, no repair is left. The file is published with the line `NOT MET`. HOLD-3 not met does not close the neuron. HOLD-4 opens when that file is on origin. When RETURN is `NOT MET`, the method file is written. The abort line is not lowered to keep an offer alive.

When RETURN is met, the families stop and the payments stop.

## HOLD-4

HOLD-4 opens when the desk's HOLD-3 file is on origin, met or not met. The sample minute is the first whole UTC minute whose start is at least 3 minutes after that file's On origin time. A file on origin at 14:07:22Z pins 14:11:00Z. A file on origin at 14:07:00Z pins 14:10:00Z. The desk and the bot both read that time from origin.

The desk samples that minute when its submit path is synced and that node's DAA is moving. If either is false, the file still covers that minute. The first line is `OBSERVATION`. One line says the path was not synced. The rate in an unsynced minute is not the sample. The run does not open a later minute. The submit-OK in a synced minute is the reading, including a rate under 3,040. The file is written after that minute. The run does not stay open to chase 4,053.

The bot is a planned sender on this step only. It sends payments, from its own coins, in that same minute. It does not send covenants. It has no local node. It uses one public node outside the desk's HOLD-3 set, and that set includes the family nodes. One process. The split stays in the local config. The config is not committed. If that config has no free synced node, the bot does not send. The observation still runs on the desk. A suspend ends the bot's sending for that minute. A wake after the pinned minute is `NO SEND` and `suspend`. The desk continues. The observation does not wait.

The bot's sender log is [counts/bot/HOLD-4.md](../counts/bot/README.md). Mini writes `TWO SENDERS` only when that file is on origin and its line is not `NO SEND`. A `NO SEND` line is `ONE SENDER` plus that one word. If the bot file and [logs/BOT-HALT.md](../logs/README.md) are both absent 10 minutes after the desk's HOLD-4 file is on origin, Mini writes `ONE SENDER` and `bot-file-absent`. Mini does not republish. The bot stops when its file is on origin. It also stops when the halt file is on origin. It does not send in RETURN. The families stay on the desk through the observation and through RETURN.

## Fees

Fixed for the whole run. Minimum relay is 100 sompi per gram. Families 1–13 pay 100. Families 14–16 pay 200. Every payment sender pays 150. The bot's payments, when it sends, are 150 as well, and they stay in the bot's own file. A submit rejected because the mempool is full is logged as full. It does not stop the sender. A submit rejected for the rate stops that sender. The rate is not raised. The miss is a line in the fix log. Waiting for the same reject to clear is not a new repair.

Label C. Payments at 150 sit between the two family cohorts. A yes for families 14–16 ahead of families 1–13, at HOLD-3 or in the HOLD-4 minute, is mostly that fee order. The 6 Oct saturated hold bought about 2 seconds at the median for 1.5×. The tail did not move. HOLD-1 is the control. A lead that is already there at HOLD-1 is not a congestion effect. The sixteen are one build: one program, one hop shape, one minter size, one token size. The family sender builds families 1–13 at 100 and families 14–16 at 200 in one process, on one node set. A single rate for the process is not a fee difference. If the funding coins are not one size, the method file says so and does not call the fee the whole cause. Storage mass can move with the rate, because the fee comes out of the funding coin. That move is the fee. At 1.2 hop/s the HOLD-4 minute holds at most about 72 hops per family, so a cohort gap in that minute is thin.

A node's priority quote is not read. A fee estimate is not read either, including a read that would not set the fee. The three fees stay fixed from T0 through RETURN.

## Funding

Recount before the 11:50 genesis. The abort line stays **2,500 coins** and **18,000 usable tKAS**. Do not lower it. Do not spend a mining coin at or above 100,000 tKAS. Do not print a balance, a key, or an id. One coin per family for the one genesis. The same lineage runs all day. Each landed hop locks about 1 tKAS. A target with no end time can use more of the lane than a timed hold. The abort line still stops the sender.

## Abort

A sender-off, pool-low, node-drop, or proc-exit stops that sender. The line goes into the fix log. Waiting for the abort line to become true again is not a new repair. A submit path that is not synced does not get a start. A minute on an unsynced path is not a clean minute. A failed submit is a reject. The desk records it as rate or full.

Tuesday's runner uses the desk node. This neuron leaves that process up until Tuesday's runner is down. Before Wednesday genesis the desk stops its node process. The chain data stays on disk. The senders submit to public TN10 nodes. The process stays stopped until the method file is on origin. Then it may be started again. The data is not deleted. The binary is not switched. An index is not turned on. There is no desk-node congestion row during the run. One health read goes in the local log before the stop, and one after the restart.

Miners stay off. A stretch under 8 merged blocks per second is recorded in Mini's file as miner-out. That stretch can still be a clean desk minute. It is not scored as a family failure. The method file places the two readings side by side. They are not averaged. The operator writes the time the miners go off. This page does not set that minute.

## What this plan does not change

Tuesday's repo, the 8 Nov rehearsal, and the 8 Nov confirmation stay on their clocks. 43b is [LATER.md](LATER.md).
