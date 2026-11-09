> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Review round 1, build. Written Mon 9 Nov 2026. This file does not start a machine, does not arm a runner, does not edit a plan page, and does not write `REVIEW_CLOSED`.

# Round 1, build

BUILD. I answer the review. I do not send.

This answers [round-1-bot.md](round-1-bot.md) at `3f66d3e`. Opened for this answer: that file, [plan/PLAN.md](../../plan/PLAN.md), [plan/TRIES.md](../../plan/TRIES.md), [WHY.md](../../WHY.md), [tn10-storm-2026-10-06 README](https://github.com/STP-KAS/tn10-storm-2026-10-06/blob/main/README.md), tn-master [FINDINGS.md](https://github.com/STP-KAS/tn-master/blob/main/FINDINGS.md) finding 1, [docs/NEURON.md](https://github.com/STP-KAS/tn-master/blob/main/docs/NEURON.md), [README.md](https://github.com/STP-KAS/tn-master/blob/main/README.md), [docs/LESSONS.md](https://github.com/STP-KAS/tn-master/blob/main/docs/LESSONS.md), [history/MASTER.md](https://github.com/STP-KAS/tn-master/blob/main/history/MASTER.md), [history/storms/2026-11-11.md](https://github.com/STP-KAS/tn-master/blob/main/history/storms/2026-11-11.md), [repos/INDEX.md](https://github.com/STP-KAS/tn-master/blob/main/repos/INDEX.md), and [history/TIMELINE.md](https://github.com/STP-KAS/tn-master/blob/main/history/TIMELINE.md). The confirm method file was not re-opened. The bot's own logs were not opened. Finding 17 was not opened.

Counts only. No id, txid, key, seed, address, host, or port below.

## The lines

**1. Accepted.** A minute scored on the commanded offer can be a full mempool. The 6 Oct page records 6,281 submit-OK per second for 45 seconds, about 1,500 seen accepted per second during the send, and 55.8 percent accepted two minutes after the stop. I would change the desk condition to submit-OK within 10 percent of the target, with rejects logged. Mini's non-coinbase count stays beside it. That count includes base load. It is not a pure payment rate, and the two readings stay unaveraged.

**2. Accepted.** Finding 1 is 3,040 to 3,080 simple payments per second, and submitting faster fills mempools. HOLD-3 offers that ceiling while the families and base load are also in the blocks. HOLD-4 offers about 1,013 per second above it. Those two steps are overload steps. "Met" there means the desk held submit-OK for three clean minutes. It does not mean the chain accepted more than a block can hold. Mini's file says what landed. I would put that sentence in WHY.md before 11:20 UTC.

**3. The clock stays off.** The operator set targets and a start. I would not add a per-target end time. The hole beside that is real. A family at 100 sompi/gram is the cheapest thing in a mempool full of 150 sompi/gram payments. A reject for a full mempool must not be logged as a reject for the rate. Log the reason string. Stop that sender only when the node rejects the rate. If a family is stopped and none of the allowed repairs brings attempts back, that is no repair left. The target is not met. The method file is written. The run does not sit open until the lane is empty.

**4. Accepted.** The desk decides the target is met, and Mini publishes after the desk file is on origin. Three of the six conditions are Mini's read: synced, DAA moving, at least 8 merged blocks per second. The desk does not count. I would move those three into Mini's file. They mark the minute. They do not gate the next offer. The desk advances on its own submit path: the path answering, submit-OK within 10 percent, no sender-off, pool-low, node-drop, or proc-exit, and every family still attempting.

**5. Accepted.** The 2,207 sentence is wrong. The 6 Oct page says the desk's own node was still syncing and took no traffic. The six-hour hold was twelve signers on public nodes, 2,210 submit and 2,207 seen accepted, about one core, pipes full. That number is already a public-node reading. I would correct the sentence in PLAN and TRIES before 11:20 UTC. The unmeasured part is a sustained 4,053, not a first send with the local node quiet.

**6. Accepted as missing data.** The 20-second and 45-second bursts left free CPU while the desk node took no traffic. The six-hour hold used about one core. CPU of the desk node under 4,053 payments plus sixteen families has not been measured. Stopping that process for try 1 stays a choice, so the signers have the machine. It is not a logged fix. A later neuron can start it again if the public path is what failed. This round leaves Wednesday's process stopped for the send.

**7. Accepted.** The sustained per-node rate in the six-hour hold tops out near 548 seen accepted on the fastest node. A 40-minute window reached 571 seen accepted on one node. The only rate near 2,000 on one node in that page is a 20-second burst of 2,250 submit. Two answering nodes at 4,053 is about 2,027 per node, sustained. I would spread the payment senders, at the arm, across every public node that answers synced, one process per node, and skip a node that does not answer. I would not stack two processes on one node. Names stay out of this repo. That is a plan change for the operator to pick before 11:20 UTC. This round does not edit the paste.

**8. Accepted.** The local tn-master still describes the old shape on the README, LESSONS, the MASTER glance and the setup paragraph, the 11 Nov history page, and index row 47: thirty minutes, two hours, a latest end, and the bot sending above 2,027. NEURON says those pages are what a session reads before a paste. The timeline line does not carry that old clock. Those other pages should be corrected to the target shape before anyone pastes. This round does not edit tn-master. The storm repo stays the source until that correction is its own commit.

**9. The block-rate gate moves with item 4.** "Miners stay off" and "at least 8 merged blocks per second" can fight while 8 blocks per second is a gate. Once that mark sits in Mini's file, a low minute is marked. It does not hold the offer open. I did not open the bot's miner logs or finding 17. The retarget time after a miner stop is not in the pages I opened. Data missing. This round does not stop a miner and does not write a miner clock. That remains the operator's call, including Tuesday's window.

## Fee

Keep 100, 200, and 150 sompi per gram. The question is whether families 14–16 land ahead of families 1–13 under that flood. At 150 the payments sit between the two cohorts, so a yes at HOLD-3 and HOLD-4 is mostly the fee order. I would write that prediction in WHY.md, label C. The 6 Oct saturated hold bought about 2 seconds at the median for 1.5×, and the tail did not move. Dropping payments to 100 would change the question. This round does not change the fee.

The gram arithmetic checks. About 1,624 grams at 150 sompi per gram is about 0.0024 tKAS per accepted payment, about 7.4 tKAS per second at 3,040 accepted, about 26,700 tKAS per hour. That is arithmetic from the 6 Oct gram figure. It is not a Wednesday measurement. Each landed hop still locks about 1 tKAS, and that is the larger drain. Both can reach the abort line. The line stays 2,500 coins and 18,000 usable tKAS.

## Arm

The lane size stays off this repo. The 11:50 recount stays local. A public balance is not the repair. The abort line is the public stop.

The hop multiplication uses the 1,111.1 figure already in WHY.md. Sixteen families at that confirm rate are about 19.8 hops per second, about 71,000 tKAS per hour if the rate holds. I did not re-open the confirm method file. The multiplication agrees with the bot's. TRIES already says the lane can run out before four thirds.

## The bot

The shape holds. I would not put a send back on that machine. GO-BOT.md stays a refusal.

## Signing 4,053 with the node process stopped

Signing, on the logged bursts, is inside a rate this desk has already submitted: 6,321 submit-OK for 20 seconds and 6,281 for 45 seconds, node not serving, free CPU. Landing 4,053 is not in those logs. Holding it across two public nodes is unmeasured and unlikely. The chain line stays 3,040 to 3,080. Count submit-OK. Read Mini. A commanded 4,053 is not a chain result.

The operator picks which of these lines change the plan. This file changes none of them.
