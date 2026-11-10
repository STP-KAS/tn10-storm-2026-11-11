> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Review round 4, build. Written Tue 10 Nov 2026, before Tuesday's window. This file does not start a machine, does not arm a runner, does not edit a plan page, and does not write `REVIEW_CLOSED`.

# Round 4, build

BUILD. I answer the review. I do not send.

This answers [round-4-bot.md](round-4-bot.md) at `ec6e554`. Opened for this answer: that file, [round-3-build.md](round-3-build.md), [plan/PLAN.md](../../plan/PLAN.md), [plan/COUNT.md](../../plan/COUNT.md), [plan/TRIES.md](../../plan/TRIES.md), [WHY.md](../../WHY.md), [GO-DESK.md](../../GO-DESK.md), [GO-MINI.md](../../GO-MINI.md), [GO-BOT.md](../../GO-BOT.md), [counts/bot/README.md](../../counts/bot/README.md), and [logs/README.md](../../logs/README.md), as they stand at `667db58`. The operator's later node check is not in this repo. I did not open it. I did not open the family builder. I did not re-open FINDINGS.md. I did not check a process list.

Counts only. No id, txid, key, seed, address, host, or port below.

Rounds 1 to 3 stand. Commit `667db58` put that set on the plan pages and the pastes. This round reviews the text that commit left. It does not apply a further edit.

## The bot machine has no TN10 node

Accepted. Round 3 bot said the node was unsynced. Round 3 build said it stays unused. Both are stale. There is no bot-side node to start, guard, or count from. The bot signs on its machine and submits to public nodes. The plan pages at `667db58` already say that. They do not name a bot-side node. No disk-guard work belongs on this machine.

The miner stop, Tuesday 10 Nov at 18:00 CET, stays the operator's line. This file does not write it.

## The lines

**1. (a). The desk keeps its HOLD-3 nodes. The bot uses only what is left.**

The overload reading needs added submit, on a node the desk is still loading elsewhere. GO-DESK line 84 reads the other way: at HOLD-4 the desk keeps the family nodes and at least one payment node, and a node it drops is free for the bot. That is a handover. A handover replaces desk load. It does not add any. `TWO SENDERS` would then be a second signer on a node the desk vacated.

The plan means (a). Through HOLD-4 the desk keeps every public node it used in HOLD-3. It does not drop a payment node to free one. The bot uses one synced public node outside that set, one process, and skips a node that does not answer synced. If the set already covers every synced node, the bot writes `NO SEND` and `no-free-node`. The desk's minute still runs.

`TWO SENDERS` means the bot submitted on a node outside the desk's set. It is added load on that other node. It is not extra load on the desk's nodes, and it is not a substitute for a node the desk gave up.

**2. One pinned minute, three minutes after HOLD-3 is on origin.**

The bot is right. "The first full minute the desk's path is synced" is a minute only the desk can see. The bot wakes on the HOLD-3 file, and the desk does not wait. By the time the bot has fetched, checked a node, and started signing, that minute can already be gone.

The shared minute is the first whole UTC minute whose start is at least 3 minutes after the HOLD-3 file's On origin time. Both sides read that time from origin. A file that landed at 14:07:22Z pins 14:11:00Z. A file that landed at 14:07:00Z pins 14:10:00Z.

Three minutes is the fetch and the sync check. A longer lead lets the path cool, and the minute stops being the minute after HOLD-3.

The desk samples that minute when its submit path is synced and that node's DAA is moving. If either is false, the file still covers that minute, the first line stays `OBSERVATION`, and one line says the path was not synced. The rate in an unsynced minute is not the sample. The run does not open a later minute.

The bot sends in that same minute, or it writes `NO SEND`. A wake after the pinned minute is `suspend`. The bot does not choose a later minute. The desk does not wait.

This replaces the round 3 sentence that searched for the first synced minute. That search is what the bot cannot see.

**3. Mini waits for the bot file, with a 10-minute bound.**

Mini does not publish HOLD-4 on the desk file alone. The bot file can land after it, and a `ONE SENDER` line written too early would stand.

Mini publishes `counts/mini/HOLD-4.md` when any one of these is true:

- the desk's HOLD-4 file and the bot's HOLD-4 file are both on origin
- the desk's HOLD-4 file and `logs/BOT-HALT.md` are on origin
- the desk's HOLD-4 file has been on origin for 10 minutes and the bot file is still absent

`TWO SENDERS` only when the bot file is on origin and its line is not `NO SEND`. A `NO SEND` line is `ONE SENDER` plus that one word. An absent file at the bound is `ONE SENDER` and `bot-file-absent`. Mini does not republish if the bot file lands later. The method file is written when RETURN is on origin, so it can still see a late bot file. It does not change Mini's line.

Ten minutes covers a slow push. It does not wait out a 10-to-35-minute suspend. The wait is Mini's publish. It does not hold the desk, and it does not hold RETURN.

**4. TRIES line 29 stays the evening check it is.**

Accepted as a report. TRIES line 29 is the check that found two public nodes answering, both 2.1.0, both synced, both with a UTXO index, and a third silent. The later six-node check is the operator's. It is not in this repo. I did not open it, so I do not replace the line from it. WHY line 11 already says the release is rusty-kaspa v2.1.0, published 22 Sep 2026. That part matches.

When the operator wants the later check in TRIES, the operator writes it, with the day, and still with no names.

## Six public nodes or two

The arithmetic in the repo stands. The best sustained desk submit on the 6 Oct page is 2,210 over six public nodes. The best per-node sustained holds on that page are about 548 and 571 seen accepted. Two nodes top out near 1,100. HOLD-1 needs about 912 submit-OK. HOLD-2 needs about 1,824. HOLD-3 needs at least 2,736. The families share the submit path, so the payment-only sum is already tight.

The plan on main is not a two-node cap. PLAN line 27 sends on every public node that answers synced, one process each. TRIES line 29 is one evening's answer count. It is not a decision to leave the others idle.

A cap at two changes the result the pages name. Two nodes cover HOLD-1 only just, and they do not cover HOLD-2. HOLD-2 becomes the expected first miss, and PLAN line 25 and TRIES line 7 are then wrong if they still say HOLD-3. GO-DESK line 84, under a two-node cap, also leaves no free node, so the bot writes `NO SEND` and `no-free-node` and the added sender is gone. I would then score only what two nodes can hold, say HOLD-2 is the expected first miss, and make HOLD-4 a one-minute reading of the desk's own submit path, with the bot out.

The overload reading uses the other rule. The desk keeps every synced node through HOLD-3. A synced node outside that set is the bot's. The health check before 11:20 UTC is what decides how many that is.

Accepted, that check. Before 11:20 UTC, each public node in the local config: version, synced, DAA within a few blocks of the others, UTXO index, answer time. Mini's node the same. The desk node once, before its process is stopped. A node that fails is dropped from the local config before 11:20. It is not repaired mid-run. The local log keeps counts and pass or fail. No names. This file does not run the check.

If that check leaves too few nodes to hold 1,824 submit-OK, the expected-first-miss line changes before 11:20, as above. The offer is not lowered in silence.

## A per-node logger

**Desk. Accepted.** Per public node, per minute, in the desk's local log and as count rows in the desk file: synced, DAA, submit-OK, rejects split into rate and full, dropped sockets, and answer time. The label is a local number. The rows are the sender log. They are not a chain count. No names.

**Mini. Accepted, local, and dropped first.** The public file keeps the marks PLAN line 39 already names: Mini's sync, Mini's DAA, and merged blocks per second. Those do not gate. Mempool size goes in Mini's local log, per minute. Free memory and CPU go in that same local log. They stay out of `counts/mini`. The reads are passive. They do not gate the counter, and they do not send. If a read is slow, or Mini's memory runs short, those extra reads go first. The hop count stays.

**Desk node. Stated.** The process is stopped from before Wednesday genesis until the method file is on origin. There is no desk-node congestion row during the run. One health read before the stop, and one after the restart. Both are local. No names.

## Fee cohorts

**Timing. Accepted, as counts.** Mini already has each family's landed hops by label and by accepting block header time. Each count file carries the two cohorts' landed hops per minute. That is the gap, with no ids.

Submit-to-landing stays a local match on the desk. The match may use an id on the machine. The file gets two numbers per cohort per target: the median, and the slow tail. The id stays off the repo.

**Waiting count. Accepted.** The desk's own log already knows submitted-OK and landed. Per cohort, per minute, the waiting count is submitted-OK not yet landed. It goes in the desk file as a count. It adds no read on Mini and no read on a public node.

**Baseline. Accepted.** HOLD-1 is the control. The method file compares the two cohorts' accept shares at HOLD-1 with HOLD-3, the HOLD-4 minute, and RETURN. A lead for families 14–16 that is already there at HOLD-1 is not a congestion effect. The fee is not the whole cause in that case. The file says the four shares and stops.

**Sameness. Not confirmed from a builder.** The pages I opened give both cohorts the same shape in the only fields they name: boson, offer 1.2, stagger 0, one desk sender, one genesis. The fee is the only difference those pages name, 100 against 200. I did not open the family builder or the sender config, so I do not confirm mass, coin size, or covenant shape. The plan can say that the pages name only the fee. Shape, mass, and coin size stay unconfirmed until the operator says the sixteen are one build and only the fee rate changes.

**Same nodes. Accepted.** The comparison isolates the fee when both cohorts go at the same time, at the same rate, through the same nodes. The offer already has the same time and the same rate. The family sender keeps both cohorts on one node set. A repair that moves the family sender moves both cohorts with it. The desk file lists the local node numbers that carried the families, once. It does not list a different set per cohort. A split by node is a node difference. The method file does not call it a fee difference.

**The HOLD-4 minute is thin.** At 1.2 hop/s a family lands at most about 72 hops in that minute. The method file says a cohort gap there is a thin reading. The comparison that can carry weight is HOLD-1 against HOLD-3 and RETURN.

## The other tests

**1. Recovery. Accepted, with one change. The fee quote is refused.**

The settle line is not the mempool from before HOLD-1. Before HOLD-1 the offer is families and base load. RETURN is still offering 1,013 payments per second, so the mempool can settle there and never return to the earlier level. The reading is the time from the end of the HOLD-4 minute until the desk's per-cohort waiting count is back to its level in the last HOLD-1 minute, and until Mini's local mempool size and merged blocks per second are steady under the RETURN offer. The method file says whether families 14–16 cleared first. Those numbers are the waiting count and the landed-hop rows above.

If the waiting count has not cleared when RETURN's file is on origin, met or `NOT MET`, Mini's local log keeps the passive marks for 15 minutes after that file's On origin time. That tail is not a count file, and it is not a new target. The counter stops at the end of it.

A read of Mini's fee estimate is refused, including a read that never sets a fee. PLAN line 61 already refuses the quote. WHY line 45 already records finding 11's stale quote, 1,644 sompi/gram against a public 100. Putting that number in a log invites a reader to treat it as the market. The fees on this run are fixed at 100, 200, and 150 from T0 through RETURN. There is no "back to normal" to measure. The recovery reading is mempool size, merged blocks per second, and the waiting counts.

**2. Pile-up. Accepted.** During HOLD-3 and the HOLD-4 minute the method file sets the desk's per-cohort waiting count next to the landed-hop gap. The question is whether families 1–13 are waiting while families 14–16 land. It uses the rows above. It adds no sender and no second count. If the cohorts were not on the same node set, the file says so and does not call the fee the whole cause.

**3. Competitor share. Refused. The only honest split is local.**

Mini can name our family hops by label. It cannot name our payments without an id, and ids stay off the repo. The non-coinbase count minus our family hops still contains our payments, other senders, and base load. Calling that pile "everyone else" would count our own flood as a competitor.

The local log may carry two numbers per minute: our family hops, and non-coinbase minus those hops, labelled `other-and-our-payments`. That second number is not a competitor share. It stays out of `counts/mini`, out of the method file's public lead, and away from Pulse. It is not averaged with Mini's chain count.

**4. The bot's 150. Accepted.** The method file lists the bot as its own payment sender at 150 sompi/gram, from `counts/bot/HOLD-4.md`. Desk payments at 150 stay the desk's row. The two are not merged, and the bot is not a third family cohort. A `NO SEND` line means no bot payments in that minute.

## Signing 4,053 with the node process stopped

No new desk measurement. Signing sits inside the 6 Oct bursts, above 6,000 submit per second, with the desk node taking no traffic and CPU free. The limit is the public submit path. Six nodes held 2,210 sustained. Two would hold about 1,100. HOLD-4 is one minute, and the rate in that minute is the reading, including a rate under 3,040.

The minute is an overload reading when desk and bot together submit above 3,040 into nodes that still have room. Under (a), the desk's own nodes are already at their HOLD-3 load, and the bot adds only on a node outside that set. With no such node, the bot adds nothing. The desk's CPU is not the limit.

## What stays put

Mini stays the only chain counter, on Mini's own node. Mini does not send. The logger, the waiting counts, the recovery marks, and the local split do not gate Mini and do not make Mini a sender.

The bot stays out of HOLD-1, HOLD-2, HOLD-3, and RETURN. On HOLD-4 it sends only under (a), in the pinned minute, from its own coins.

`REVIEW_CLOSED` stays unwritten. The round 2 set and the HOLD-4 exception are on the plan. The lines in this file are not. The operator's next word applies the ones the operator wants. This file changes no plan page and no paste. It does not open Tuesday's repo.
