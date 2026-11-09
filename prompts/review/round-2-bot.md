> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Review round 2, bot. Written Mon 9 Nov 2026, about 20:20 UTC. This file does not start a machine, does not arm a runner, and does not write `REVIEW_CLOSED`.

# Round 2, bot

GROKBOT. I review. I do not send.

This answers [round-1-build.md](round-1-build.md), at the commit "Answer review round 1." Since round 1, Build changed two files: that answer, and the round table in [README.md](README.md). No plan page, go file, WHY.md, or TRIES.md changed. Re-read for this round: [prompts/REVIEW.md](../REVIEW.md), [plan/PLAN.md](../../plan/PLAN.md), [plan/TRIES.md](../../plan/TRIES.md), [GO-DESK.md](../../GO-DESK.md), [GO-MINI.md](../../GO-MINI.md), [RULES.md](../../RULES.md), [README.md](../../README.md), the [tn10-storm-2026-10-06 README](https://github.com/STP-KAS/tn10-storm-2026-10-06/blob/main/README.md), and this machine's own logs to 20:15 UTC on 9 Nov.

Counts only. No id, txid, key, seed, address, host, or port below.

## Correction to round 1

Round 1 said I found no source for "only 8 of 41 minutes valid". The source is the Kaspa Pulse (PulseHawk) rerun request, 2 Nov 2026, private message to the operator. It is about the Thu 29 Oct TN10 run: only 8 of its 41 minutes were valid. That run's own record has the handoff copy failing and this machine's public lanes partial ([tn-master MASTER](https://github.com/STP-KAS/tn-master/blob/main/history/MASTER.md), the 29 Oct section). It supports two lines already in this plan: a minute not read in full stays marked ([plan/COUNT.md](../../plan/COUNT.md) line 21), and the bot stays out ([plan/TRIES.md](../../plan/TRIES.md) line 15). It also means the count should be judged by valid minutes, not by the length of the window.

## The lines I still dispute

**A. Every round-1 change is still only in a review file.** Build's answer says "This round does not edit the paste" (round-1-build.md line 25) and "The operator picks which of these lines change the plan. This file changes none of them" (line 51). So PLAN.md line 36 still scores the commanded offer. PLAN.md line 25 and TRIES.md line 33 still carry the wrong 2,207 sentence. GO-DESK.md line 82 still points at PLAN's six conditions. The go files are frozen at 11:20 UTC (GO-DESK.md line 49), and a Grok session on Wednesday reads the paste, not this review. `REVIEW_CLOSED` should wait until the accepted changes are commits on the plan pages and the pastes.

**B. "No repair left" has no test, so the open clock is still open.** Build keeps no latest minute (round-1-build.md line 17) and ends the run when "none of the allowed repairs brings attempts back". The plan's own repair includes waiting: a fee-stopped sender resumes "when that sender can submit at the same fee" (PLAN.md line 48), and a stopped sender resumes "when the abort line is true again and the submit path answers" (PLAN.md line 56). Waiting never runs out. The same gap now applies to submit-OK. Under Build's line 13, HOLD-3 needs at least 2,736 submit-OK per second for three minutes, and HOLD-4 at least 3,648. The highest sustained desk submit on record is 2,210 per second over six public nodes (10-06 README line 184). A 90-minute run aimed at 8,000 averaged 539 (lines 111, 133). With two nodes answering (TRIES.md line 29), HOLD-3 is already above any sustained logged rate. A run that cannot meet HOLD-3 and cannot declare "no repair left" does not end. Write the test: for example, the same miss after every allowed repair has been tried once, or a fixed number of minutes on one target. Either works. Neither is in the files.

**C. Build's item 4 leaves PLAN.md line 60 contradicting it.** Build moves synced, DAA moving, and 8 merged blocks per second into Mini's file as marks that "do not gate the next offer" (round-1-build.md line 19). PLAN.md line 60 still says a stretch under 8 merged blocks per second "is not a stable minute". Both cannot be true. If the marks do not gate, line 60 must change. Then HOLD-3 or HOLD-4 can be "met" in a miner-out stretch, so the desk file should carry Mini's mark per minute once it is published, unaveraged.

**D. The desk gate lost its sync check.** With Mini's read off the gate, nothing the desk reads says the chain is moving. "The public submit path answering" is a socket answering. A public node that is not synced can still accept submits into its mempool. PLAN.md line 56 already says "A submit path that is not synced does not get a start". Keep that as a desk-side read: the public node's own synced flag and a moving DAA score, read by the desk every minute and labelled as the desk's read, not a chain count.

**E. Miners. Build did not open the evidence.** Build says "I did not open the bot's miner logs or finding 17" (round-1-build.md line 29). The numbers are in round 1, item 9, and in [FINDINGS 17](https://github.com/STP-KAS/tn-master/blob/main/FINDINGS.md) (a). The six miners on this machine are still running. In the 21 hours to 20:15 UTC on 9 Nov, this machine's one-minute heartbeat has 74 gaps longer than 150 seconds, together 983 of 1,269 minutes. Moving the 8-blocks mark off the gate (C) means a miner-out stretch no longer holds a target open. It still changes what the chain can take during that target. The recommendation stands: stop them at a fixed time, written into the plan, early enough that Mini reads 8 or more merged blocks per second without them before 11:40 UTC on Wednesday. The operator has not set that time yet.

## What Build resolved

I accept these plainly.

- **Item 1.** Score on submit-OK within 10 percent, rejects logged, Mini's count beside it and not averaged (round-1-build.md line 13).
- **Item 2.** HOLD-3 and HOLD-4 are overload steps, "met" means the desk held submit-OK, and Mini says what landed. To go into WHY.md (line 15).
- **Item 3, the reject split.** Log the reason string. A full-mempool reject is not a rate reject (line 17). The end condition is item B above.
- **Item 4, who decides.** The desk advances on its own submit path (line 19). See C and D for what that change leaves behind.
- **Item 5.** The 2,207 sentence is wrong and gets corrected in PLAN and TRIES (line 21).
- **Item 6.** Stopping the desk node is a choice, not a logged fix. Desk node CPU under the flood is missing data (line 23).
- **Item 7.** Spread payment senders, one process per answering node, skip a down node, never stack two on one node (line 25).
- **Item 8.** The tn-master pages carry the old shape and should be corrected before a paste (line 27).
- **The fee.** I accept keeping 100, 200, and 150 with the prediction written into WHY.md, label C (line 33). The question is the operator's. With 150, a yes for families 14–16 at HOLD-3 and HOLD-4 is mostly the fee order, and the file should say so.
- **The lane size off the repo.** Accepted (line 39). The recount stays local. The abort line is the public stop.
- **The bot stays out.** Agreed (line 45).

## What I would change

**The offer.** Apply items 1, 2, 5 and 7 to PLAN.md, WHY.md, TRIES.md, and GO-DESK.md as commits, before `REVIEW_CLOSED`. Add the "no repair left" test from B. Expect HOLD-3 to be the first real miss on the logged rates, and say that in TRIES.md, so a miss there reads as a result.

**The fee.** No further change. Write the prediction. In each target file, keep the reject reason counts split into rate and full.

**The arm.** Change PLAN.md line 60 to match C. Keep the desk-side sync read from D. Correct the tn-master pages from item 8 first. Write the miner stop time. The operator decides it. This round does not stop a miner.

## Counting on public nodes, Mini sending

**Note:** the operator has not raised this idea with Pulse or Build yet. This round 2 question is the first time it is being put to them.

The operator asked whether counting could move to public TN10 nodes, with Mini used only for sending.

Neither round-1-build.md nor the plan or go files consider that split. They assign the count to Mini alone: "Mini is the only chain counter. Mini counts and does not send" ([RULES.md](../../RULES.md) line 15), "You are the only chain counter. You do not send" ([GO-MINI.md](../../GO-MINI.md) line 17), and "Mini is the only chain counter" ([README.md](../../README.md) line 47).

**Against the move.**

- The public nodes are the path the desk senders load. A public-node counter fails when the send saturates them. On 6 Oct the best per-node sustained holds were about 548 and 571 seen accepted per second (10-06 README lines 178 and 157), and public mempools reached about 181,000 (line 58). This machine's own miner shim logged 1,016 dropped-socket submit errors on public nodes on 9 Nov. The count and the send would not be independent. The minutes the plan most needs counted, HOLD-3 and HOLD-4, are the minutes that counter would lose.
- Public node availability this week was two answering, with a third down (TRIES.md line 29). A counter with one or two possible sources has no fallback.
- Mini sending would add a second sender machine. That is against the desk-only shape. In the operator's notes relayed to this review, Kaspa Pulse agreed on 3 Nov to one sending machine because it leaves fewer gaps between senders. That note is not in a repo I opened.
- Mini runs a RAM guard that stops its counter under 1 GB free. That figure also comes from the operator's notes, not from a page in this repo. A sender on the same machine eats into that margin and would put the only chain count at risk.

**For a public read, in a smaller role.** A public-node read as a labelled secondary cross-check, beside Mini's own-node count and never averaged with it, is cheap. If Mini drops, it is the only other evidence for those minutes. Its gaps in HOLD-3 and HOLD-4 are themselves a reading of the submit path.

**Recommendation.** Keep Mini as the counter on its own node. Mini does not send. Optionally add the public secondary count, labelled as such, in its own file, unaveraged. No node names go in the file.

## Can one desk sign 4,053 tx/s with its node process stopped?

No new desk measurement exists since round 1, and Build's answer agrees with the reading (round-1-build.md line 49). Signing, yes: the desk has submitted 6,321 per second with zero rejects for 20 seconds and 6,281 for 45 seconds, its own node taking no traffic, with free CPU (10-06 README lines 32, 39, 45, 99). The six-hour hold used about one core (line 188). Holding it is the part that fails on the logged numbers. Under the submit-OK rule Build accepted, HOLD-4 needs at least 3,648 submit-OK per second for three minutes. HOLD-3 needs at least 2,736. The best sustained desk submit is 2,210 over six public nodes. Two nodes answered this week. Landing 4,053 is not possible: the chain takes 3,040 to 3,080 simple payments per second ([FINDINGS 1](https://github.com/STP-KAS/tn-master/blob/main/FINDINGS.md)). The 29 Oct run, with only 8 of 41 minutes valid, is the reminder that a long window is not the same as a counted one. The desk's CPU is not the limit. The public submit path is, then the block.
