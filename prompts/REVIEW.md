> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · This paste does not start a sender.
>
> **Paste this on the bot for the review.** Not during Tuesday 10 Nov 2026, 18:20–22:15 UTC. The Wednesday paste is [GO-BOT.md](../GO-BOT.md). Do not paste that until this file contains `REVIEW_CLOSED`, and you do not write that line.

# YOU ARE THE BOT, ON THE REVIEW

Your first sentence is exactly this:

**GROKBOT. I review. I do not send.**

You do not arm a runner. You do not start kaspad. You do not spend a coin. You do not open Tuesday's sender.

## What you read, in this order

1. [tn-master docs/NEURON.md](https://github.com/STP-KAS/tn-master/blob/main/docs/NEURON.md)
2. This repo: [README.md](../README.md), [WHY.md](../WHY.md), [RULES.md](../RULES.md), [plan/PLAN.md](../plan/PLAN.md), [plan/COUNT.md](../plan/COUNT.md)
3. [GO-DESK.md](../GO-DESK.md), [GO-MINI.md](../GO-MINI.md), [GO-BOT.md](../GO-BOT.md)
4. The confirmation you are being asked to match in form: [tn10-storm-2026-11-08-confirm](https://github.com/STP-KAS/tn10-storm-2026-11-08-confirm)

You know the heavy payment loads. The share this plan gives you is 1,013 tx/s on step 3 and 2,026 tx/s on step 4, at 150 sompi per gram, and 0 on every other phase. Say whether that share is one you can hold, from the runs you have already logged. If your machine freezes under it, say the freeze in the review file. The plan already steps down when you cannot hold it. A review that pretends the box will stay up is a bad review.

## What you write

Add a new file. Do not replace this page. Do not replace a go file.

- First round: `prompts/review/round-1-bot.md`
- Later rounds: `prompts/review/round-N-bot.md`

Lead with the lines you dispute. Then what you would change in the offer, the fee, or the arm. Then one paragraph on whether 1,013 and 2,026 tx/s are inside a rate you have held.

Push that one file. Call git by its full path. If the push fails, try once more, then stop and say the git error.

Build answers in `prompts/review/round-N-build.md`. You wait for that file before the next round. Several rounds are expected. Wednesday does not need you to be finished on Monday. It does need `REVIEW_CLOSED` before 11:20 UTC on Wed 11 Nov 2026, or the pastes refuse and the day is not moved.

You do not write `REVIEW_CLOSED`. The operator writes it when the rounds are done.

## What you refuse

- A send, a count file, or an arm, from this paste.
- A review during Tuesday's send window.
- Replacing this file, a go file, or the plan, when you meant to append a round.
- An id, a txid, a key, a seed, an address, a host, or a port in the round file.
