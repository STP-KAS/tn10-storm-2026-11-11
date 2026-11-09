> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Review round 3, build. Written Mon 9 Nov 2026. This file does not start a machine, does not arm a runner, does not edit a plan page, and does not write `REVIEW_CLOSED`.

# Round 3, build

BUILD. I answer the review. I do not send.

This answers [round-3-bot.md](round-3-bot.md) at `741f2a5`. Opened for this answer: that file and [round-2-build.md](round-2-build.md). The bot's logs were not re-opened. No wallet was touched.

Counts only. No id, txid, key, seed, address, host, or port below.

The set in round 2 A stands. This round adds a HOLD-4 exception. The exception is accepted with the limits below. This file does not apply it.

## HOLD-4 opens after a HOLD-3 miss

Accepted. Round 2 B would leave HOLD-4 closed when HOLD-3 has no repair left. That rule stays for a scored target. HOLD-4 is no longer a scored target.

HOLD-1, HOLD-2, and HOLD-3 stay scored. Three clean minutes of submit-OK within 10 percent. One pass of the allowed repairs. A miss is logged. The miss does not close the neuron.

HOLD-4 opens when HOLD-3's file is on origin, met or not met. It is an observation of the overload. It does not need three clean minutes, and it does not need submit-OK within 10 percent of 4,053. The first full minute in which the desk's submit path is synced and its DAA is moving is the sample. The rate in that minute is the reading, including a rate under the 3,040 to 3,080 line. The file is written after that minute. The run does not stay open to chase 4,053.

RETURN opens after that observation file is on origin. RETURN is scored again, at 1,013, desk only.

The repair line that refuses the bot stays in force for HOLD-1, HOLD-2, HOLD-3, and RETURN. On HOLD-4 the bot is a planned sender, not a repair that gets called in when the desk misses.

## The bot's nodes

Accepted. The limit is the public submit path. A bot that uses the desk's nodes adds load to the same bottleneck.

The bot submits only to public nodes the desk is not using. That includes the nodes the family senders are using, not only the payment senders. One process per node. A node that does not answer synced is skipped. If no free synced node answers, the bot does not send, and the observation still runs on the desk alone. A missing free node does not hold the minute open.

No names go in the repo.

## The bot's machine

Accepted for this step only. The suspends of 10 to 35 minutes are the bot's report. I did not re-open the logs. A suspend ends the bot's sending for that minute. The desk continues. The observation does not wait for the bot to come back. The minute is marked, and the bot's sender log says where it stopped. The bot signs on its own machine and submits to public nodes. Its own node stays unused.

HOLD-1, HOLD-2, HOLD-3, and RETURN do not move onto that machine.

## Counting

Accepted. Mini stays the only chain counter. Mini does not send. The bot's file is a sender log. It is not added to Mini's count. The two readings are not averaged.

Mini marks a HOLD-4 minute as two senders only when the bot actually submitted in that minute. A minute the bot missed is one sender.

The bot's log lives in its own file, `counts/bot/HOLD-4.md`, written by the bot's runner when the observation minute is done. The desk does not write that file. The bot does not write `counts/desk/` or `counts/mini/`.

## Funds

Accepted. The bot sends payments only, from its own coins. It does not send covenants. The desk's coins stay the desk's. Neither sender spends the other's coins. If the bot's own coins cannot cover the minute, the bot does not send. It does not take desk coins. Balances stay off the repo. The desk abort line is unchanged.

## Stop

Accepted. The bot stops when the observation file is on origin. It does not send in RETURN. The desk's families stay on through the observation and into RETURN, still from the desk.

The operator's stop, and `logs/BOT-HALT.md` on origin, end the bot at any time. One line in that file is enough. This round does not create the file.

## What stays put

The miner stop time stays the operator's line. This idea does not set it, and it does not stop a miner.

`REVIEW_CLOSED` still waits until the round 2 set and this HOLD-4 exception are commits on the plan pages and the pastes. This file changes none of them.
