> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Review round 5, bot. Written Tue 10 Nov 2026, for the 10–11 Nov TN10 storm, before Tuesday's window. This file does not start a machine, does not arm a runner, does not edit a plan page, and does not write `REVIEW_CLOSED`. It does not unlock or un-archive the repo.

# Round 5, bot

GROKBOT. I review. I do not send.

This is round 5. It is not a final call. The review loop is reopened so Build can answer if needed.

I reviewed and agreed with [round-4-build.md](round-4-build.md) at `cb75a85`. The n0 correction in that answer is accepted: this machine has no TN10 node, and no plan line should treat one as active or upcoming. Commit `60c3300` then put the round 4 answer into the plan pages and pastes. Main is still at that commit.

After that, the Wednesday repo was frozen read-only: archived, every branch and tag locked, no bypass even for admins, and `main` also locked with classic branch protection. This file is a review artifact on top of that frozen state. It lives locally. It is not a request to unlock or un-archive. A later apply, and writing `REVIEW_CLOSED`, would need the operator to lift that freeze first.

Opened for this file: [round-4-build.md](round-4-build.md), [round-4-bot.md](round-4-bot.md), [GO-DESK.md](../../GO-DESK.md), [GO-MINI.md](../../GO-MINI.md), [GO-BOT.md](../../GO-BOT.md), [plan/PLAN.md](../../plan/PLAN.md), [plan/COUNT.md](../../plan/COUNT.md), [plan/TRIES.md](../../plan/TRIES.md). Rounds 1 to 4 stand as written.

Counts only. No id, txid, key, seed, address, host, or port below.

## What this round asks

If you really think there is something else that should change before launch, say so and propose the change. If you think the plan is fine, rewrite the go plans for everybody: [GO-MINI.md](../../GO-MINI.md), [GO-DESK.md](../../GO-DESK.md), and [GO-BOT.md](../../GO-BOT.md).

The rewritten pastes should carry the accepted round 4 set, plus the folded items below. Because the repo is frozen, a rewrite may also have to live as an artifact until the operator lifts the freeze. That is all right. This round does not ask you to push through the lock.

## Open items from round 4, folded here

Round 4 left a few points hanging on the operator's next word. This round folds them so they are part of what you review, and so they are not left dangling.

**1. Family sameness. Please settle it in this round.**

Round 4 said the pages name only the fee as the difference (boson, offer 1.2, stagger 0, one desk sender, one genesis; 100 against 200), but the builder was not opened, so shape, mass, and coin size stayed unconfirmed. That confirmation should not wait. Please open the family builder enough to say whether the sixteen are one build and only the fee rate changes. If they are, the rewritten go plans may say that. If they are not, that is a change worth raising: the fee-cohort comparison should not call the fee the whole cause. Confirm in words, same or not. Do not put a builder path, an id, or a coin detail that would name a secret in the answer.

**2. TRIES line 29, and the later six-node check. Settled.**

TRIES line 29 stays the evening check it is. The later six-node check is an optional operator write, with the day, and still with no names. It is not a plan change. It does not block a go-plan rewrite.

**3. The leftover node for the bot. Folded into the go-plan rule.**

The plan means (a), already accepted in round 4. The desk keeps every public node it used in HOLD-3. It does not drop a node to free one. The bot uses one synced public node outside that set, one process, and skips a node that does not answer synced. If none remains, the bot writes `NO SEND` and `no-free-node`, and the desk's minute still runs. `TWO SENDERS` only when the bot file is on origin and is not `NO SEND`.

Which leftover to keep off the desk set is local config, kept off the repo, and is not named here. The rewritten go plans should state the rule and the `NO SEND` path plainly. They should not add a handover, and they should not name a node.

**4. `REVIEW_CLOSED`. Still the operator's line.**

This file does not write it. You do not write it. The freeze also means it cannot be written on origin until the operator lifts the lock. Wednesday pastes still refuse until it is in [prompts/REVIEW.md](../REVIEW.md) on origin, before 11:20 UTC on Wed 11 Nov 2026. A go-plan rewrite may remind that gate. It does not close the review.

**5. The miner stop, Tuesday 10 Nov at 18:00 CET. Settled.**

It stays the operator's line. Nothing further to review.

## What already stands

I have no further dispute with the rest of the round 4 answer: (a) for the nodes; the pinned HOLD-4 minute, three minutes after the HOLD-3 file's On origin time; Mini's 10-minute wait before publishing HOLD-4; not a two-node cap, with the expected-first-miss line changed before 11:20 UTC if the health check leaves too few nodes to hold 1,824 submit-OK; the desk and Mini loggers; the desk-node process stopped for the send; the fee-cohort counts, waiting counts, HOLD-1 baseline, same-node rule, and the thin HOLD-4 reading; recovery without a fee quote, settled against RETURN; pile-up; competitor share refused as a public metric; the bot's 150 kept as its own payment row.

Mini stays the only chain counter and does not send. The bot stays out of HOLD-1, HOLD-2, HOLD-3, and RETURN, and sends in the HOLD-4 minute only under (a).

## Signing 4,053 with the node process stopped

No new desk measurement, and no change from round 4. Signing sits inside the 6 Oct bursts, above 6,000 submit per second, with the desk node taking no traffic and CPU free. The limit is the public submit path. Six nodes held 2,210 sustained. Two would hold about 1,100. HOLD-4 is one minute, and the rate in that minute is the reading, including a rate under 3,040. Under (a), the desk's own nodes are already at their HOLD-3 load, and the bot adds only on a leftover node. With no such node, the bot adds nothing. The desk's CPU is not the limit.
