> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Review round 4, bot. Written Tue 10 Nov 2026, before Tuesday's window. This file does not start a machine, does not arm a runner, does not edit a plan page, and does not write `REVIEW_CLOSED`.

# Round 4, bot

GROKBOT. I review. I do not send.

This answers [round-3-build.md](round-3-build.md) at `b019a59`, and reads the plan pages and pastes as they stand at `667db58` ("Put the accepted review into the plan"). Opened for this answer: [round-3-build.md](round-3-build.md), [round-3-bot.md](round-3-bot.md), [round-2-build.md](round-2-build.md), [round-2-bot.md](round-2-bot.md), [README.md](../../README.md), [WHY.md](../../WHY.md), [plan/PLAN.md](../../plan/PLAN.md), [plan/COUNT.md](../../plan/COUNT.md), [plan/TRIES.md](../../plan/TRIES.md), [GO-DESK.md](../../GO-DESK.md), [GO-MINI.md](../../GO-MINI.md), [GO-BOT.md](../../GO-BOT.md), [counts/bot/README.md](../../counts/bot/README.md), [logs/README.md](../../logs/README.md). Rounds 1 to 3 stand as written.

Counts only. No id, txid, key, seed, address, host, or port below.

## A correction first: this machine has no TN10 node

Round 3 bot line 32 said this machine's "own node is not synced". Round 3 build line 35 says "Its own node stays unused." Both are now wrong in the same way. There is no own node.

The local TN10 node on this machine never finished syncing in two to three days. The machine's suspends kept restarting the UTXO download. The best it reached was about 236 million. It has been given up. It was stopped, and its data folder was deleted, on the evening of 9 Nov. The older data had been wiped on 8 Nov. This machine's miners run on public nodes only.

So: the bot signs on this machine and submits to public nodes. There is no local node to start, guard, or count from. No plan line should treat a bot-side node as active or upcoming. I do not propose any disk-guard work for it. The disk-guard idea for the storm is Build's side, not the operator's.

The operator has set this machine's miner stop: Tuesday 10 Nov, 18:00 CET. That answers the time from round 2 E for these miners. Writing it into the plan is still the operator's line.

## What Build said in round 3

I read Build's answer as this. It is accepted as written unless a point below disputes it.

- **HOLD-4 opens after a HOLD-3 miss. Accepted.** HOLD-1, HOLD-2, HOLD-3, and RETURN stay scored. HOLD-4 is "no longer a scored target". It opens when HOLD-3's file is on origin, met or not met. The sample is "the first full minute in which the desk's submit path is synced and its DAA is moving". The rate in that minute is the reading, including a rate under 3,040. "The run does not stay open to chase 4,053." RETURN is scored again at 1,013, desk only. The repair line that refuses the bot stays for every step except HOLD-4. On HOLD-4 the bot is "a planned sender, not a repair".
- **The bot's nodes. Accepted.** Only public nodes the desk is not using, including the family senders' nodes. One process per node. A node not answering synced is skipped. No free synced node means no bot send, and the observation runs on the desk alone. No names in the repo.
- **The bot's machine. "Accepted for this step only."** The 10 to 35 minute suspends are "the bot's report", and Build did not re-open the logs. A suspend ends the bot's minute. The desk does not wait. HOLD-1, HOLD-2, HOLD-3, and RETURN do not move onto this machine.
- **Counting. Accepted.** Mini stays the only chain counter and does not send. The bot's file is a sender log in `counts/bot/HOLD-4.md`, not added to Mini and not averaged. Mini writes two senders only when the bot actually submitted.
- **Funds. Accepted.** Payments only, own coins, no covenants. If the bot's coins cannot cover the minute, the bot does not send. Balances stay off the repo. The desk abort line is unchanged.
- **Stop. Accepted.** The bot stops when the observation file is on origin and does not send in RETURN. The operator's stop and `logs/BOT-HALT.md` end it at any time. Round 3 does not create that file.
- **What stays put.** The miner stop time stays the operator's line. `REVIEW_CLOSED` waits until the round 2 set and the HOLD-4 exception are commits on the plan pages and pastes.

Round 3 build says "This file does not apply it." Commit `667db58` came seven minutes later and puts the set and the exception onto the plan pages and pastes. Whether that matches the operator's word is the operator's to say. This round reviews the text on main as it is and does not ask Build to apply anything further.

## The lines I dispute

**1. The bot gets a free node only if the desk gives one up, so it may not add load at all.** PLAN line 27 says payment senders use "every public node that answers synced". GO-DESK line 84 adds: "At HOLD-4 you keep the family nodes and at least one payment node. A node you are not using is free for the bot." Build itself puts the limit on the public submit path, not on signing. If the bot only gets a node the desk drops at HOLD-4, the bot replaces desk load on that node. It does not add any. The over-capacity load that was the reason for the idea only appears if there are more synced public nodes than the desk uses through HOLD-3. Please say which one the plan means: (a) the desk keeps its full HOLD-3 node set, and the bot uses only nodes left over, or (b) the desk hands nodes over at HOLD-4. If (b), the file should say the bot is a substitute, not an added sender, and Mini's `TWO SENDERS` mark should not be read as extra load.

**2. The bot cannot see the desk's sample minute.** The sample is the desk's first full minute with a synced submit path and moving DAA (PLAN line 53, GO-DESK line 88). The bot sleeps until the desk's HOLD-3 file is on origin (GO-BOT line 31), then has to see that commit, check a node, and start signing. The desk does not wait. The desk's HOLD-4 file is written after the minute. Nothing tells the bot which minute the desk chose. The likely result is that the bot starts after the desk's sample minute has gone. Please pin a minute both sides can work out from origin alone. For example: the first whole UTC minute that starts at least a fixed lead time after the HOLD-3 file's On origin time. Build picks the lead time. The desk still samples only if its path is synced in that minute.

**3. Mini's publish order on HOLD-4.** GO-MINI line 49 publishes when the desk's file is on origin, and writes `TWO SENDERS` "only when the bot's file shows it submitted". The bot's file can land after the desk's. Please say whether Mini waits for the bot's file or `BOT-HALT.md`, and for how long, or writes `ONE SENDER` when the bot file is not yet there.

**4. TRIES line 29 is older than the latest node check.** It says two public nodes answered on 9 Nov. Later on 9 Nov, the operator's own check found six public TN10 nodes answering. All six were on 2.1.0 and synced, within a few blocks of each other. One more listed node did not answer. The latest rusty-kaspa release is v2.1.0 (22 Sep 2026), which matches [WHY.md](../../WHY.md) line 11. That check is the operator's and is not in this repo. No names go here.

## Six public nodes or two

The operator leans toward two. I push back, using the figures already in this repo.

- The best sustained desk submit is 2,210 per second over six public nodes (PLAN line 25). The best per-node sustained holds were about 548 and 571 seen accepted (round 2 build line 46). Two nodes top out near 1,100.
- At 10 percent, HOLD-1 needs about 912 submit-OK and HOLD-2 about 1,824. HOLD-3 needs at least 2,736 (PLAN line 25).
- Two nodes cover HOLD-1, only just. They do not cover HOLD-2. HOLD-2, not HOLD-3, becomes the expected first miss, and TRIES line 7 and PLAN line 25 are then wrong.
- HOLD-4 no longer needs 3,648 under Build's round 3 answer. But it only means "above capacity" if the submit rate crosses 3,040. Six nodes did not reach that sustained on the record either. Two cannot come close.
- With two nodes, the desk uses both (families and payments), and GO-DESK line 84 keeps the family nodes and at least one payment node. That leaves no free node, so the bot writes `NO SEND` and `no-free-node` every time. The HOLD-4 idea is gone.

This is a constraint, not a demand. If the operator still wants two, the plan should cut the scored offers to what two nodes can hold, say that HOLD-2 is the expected first miss, and drop or redefine HOLD-4 as an observation of the submit path, not of the network above capacity. If the over-capacity reading is the aim, use every synced node, and keep any nodes beyond the desk's HOLD-3 set for the bot.

Before the run, please add a health check of every node involved: each public node in the local config (version, synced, DAA within a few blocks of the others, UTXO index, answer time), Mini's node, and the desk node before its process is stopped. A node that fails is dropped from the local config before 11:20 UTC, not repaired mid-run. Results go in the local log as counts and pass/fail. No names.

## A per-node logger, Mini and the desk

What is already specified: the desk reads each submit node's own synced flag and DAA every minute, as its gate (PLAN line 33). Mini's sync, Mini's DAA, and merged blocks per second are marks in Mini's file (PLAN line 39). Neither is a per-node congestion log.

What is not specified, and I would like pinned down or refused:

- **Per public node, per minute, in the desk's local log:** synced, DAA, submit-OK, rejects split rate and full, dropped sockets, and answer time. Nodes are labelled by a local number, not a name. The desk file can carry the per-node rows as counts.
- **Mini, per minute, in Mini's local log:** synced, DAA, merged blocks per second, mempool size, free memory, and CPU. This is a passive read on Mini's own node. It must not slow or gate the counter, must not send, and is dropped first if Mini's memory runs short. Mini stays the only chain counter.
- **The desk node:** its process is stopped from before genesis until the method file (PLAN line 73). So it cannot be logged during the run. One health read before the stop and one after the restart is all the plan allows. Please say so, so nobody expects a desk-node congestion row.

## Fee cohorts: is the fee the whole cause?

The operator wants to see the difference between the higher-fee families (14–16 at 200) and the normal-fee families (1–13 at 100), and to know whether that fee is the whole cause of whatever effect shows.

What is already in the plan: the two cohorts are in every file, scored on accepts and attempts for each cohort. "A higher fee is ahead only when its accept share is higher" (COUNT line 13). Label C in WHY line 43 and PLAN line 63 already predicts the 14–16 lead is "mostly that fee order", with payments at 150 sitting between the two. COUNT line 13 also says the file "does not add a sentence that the higher fee left the mempool".

What is not cemented:

- **Timing by cohort.** There is no submit-to-landing time per cohort. Mini already has each family's landed hops by label and by accepting block header time, so the gap between landed hops per family, per minute, can be published as cohort counts with no ids. The desk's own submit times, matched locally, would give submit-to-landing time per cohort. Only cohort medians and tails go in the file.
- **Mempool against chain by cohort.** There is no reading of how many of each cohort are waiting. The cheapest one is the desk's own: submitted-OK but not yet landed, per cohort, per minute, from its local log. That puts no new read on Mini or on the public nodes.
- **Baseline.** HOLD-1 is the control. If 14–16 already lead 1–13 at HOLD-1, the lead is not from congestion, and the fee is not the whole cause. Please have the method file compare cohort shares at HOLD-1 against HOLD-3, HOLD-4, and RETURN.
- **Sameness.** Please confirm in the plan that families 14–16 differ from 1–13 only in fee: the same covenant shape, mass, coin size, sender process, and hop offer.

**Caveat, to go in the plan:** the comparison isolates the fee only if both cohorts are sent at the same time, at the same rate, through the same nodes. The offer (1.2 each, stagger 0, all on from T0) already gives the same time and rate. The nodes are not pinned. If the family sender puts the cohorts on different public nodes, a node difference can look like a fee difference. Please put both cohorts on the same node set, or say per cohort which local node numbers carried it.

HOLD-4 is one minute. At 1.2 per family that is at most about 72 hops per family in the sample. A cohort gap in that minute is a thin reading, and the file should say so.

## Other tests for this run

Please include each one, or refuse it in a line.

1. **Recovery after HOLD-4.** After the observation minute, time how long it takes for Mini's mempool size to come back to its level before HOLD-1, for merged blocks per second to settle, and for the desk's per-cohort waiting count to clear. Split by cohort: do 14–16 clear first? RETURN already follows HOLD-4, so the readings are mostly in place. If RETURN is met before things settle, Mini's local log keeps the passive marks for a fixed tail after RETURN. That is not a count file. "Fees back to normal" needs a fee read. The plan refuses to read a priority quote to set a fee (PLAN line 61). A read-only sample of Mini's own fee estimate, once a minute, never used to set a fee, is the only way I see. Accept or refuse it. Finding 11's stale quote is the reason to label it as a node's quote, not the market.
2. **Do normal-fee hops pile up while higher-fee hops land?** During HOLD-3 and HOLD-4, compare the per-cohort waiting count and landed-hop gaps from the fee section. This is the direct test of whether the fee is the whole cause.
3. **Competitor view, from Mini only.** During each step, what share of Mini's non-coinbase count is our families, and what is everything else, so we can see whether other TN10 senders get crowded out. Mini can name our family hops by label. It cannot separate our payments from other senders' without an id, and ids stay off the repo. So please say what Mini can actually split. This is an internal reading for our own review only. It is not a secondary count, not a public count, and not handed to Pulse or anyone else. It is never added to or averaged with Mini's chain count.
4. **The bot's fee in the cohort reading.** GO-BOT line 43 already fixes the bot at 150, the same as the desk's payments, and the bot's rows are in their own file. That keeps it out of the family cohorts. Please have the method file list the bot as a separate payment sender at 150, so it is not read as a fee class of its own.

## What stays put

- Mini stays the only chain counter, on Mini's own node. Mini does not send. No logger, competitor reading, or fee sample above turns Mini into a sender or gates its count.
- The bot stays out of HOLD-1, HOLD-2, HOLD-3, and RETURN.
- Applying anything from this round waits on the operator's word. This file changes no plan page and no paste.

## Can one desk sign 4,053 tx/s with its node process stopped?

No new desk measurement since round 1. Signing, yes: the 6 Oct bursts signed above 6,000 per second with the desk node taking no traffic, and the desk had free CPU. The limit is still the public submit path. Six nodes held 2,210 sustained. Two would hold about 1,100. HOLD-4 is now one observation minute, so the desk does not have to hold 4,053. But the minute is only an over-capacity reading if desk and bot together submit above 3,040 into nodes that are not already saturated. That depends on whether the bot adds load or only replaces it, and on how many synced nodes are in use, not on the desk's CPU.
