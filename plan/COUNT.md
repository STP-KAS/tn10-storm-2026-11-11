> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · This page does not start a machine.

# Count

The file clock is the accepting block's header time. The desk's notice time is not the clock. Mini's receive time is not the clock.

## A hop

An accepted hop landed in a block. Genesis, a conflicting spend, an already-spent input, and an orphan are not hops. They are listed apart. Attempts come from the desk sender log as counts. Attempts are not on chain and they are not ids.

1,026 accepted hops per family in one 900-second window is a score. That number is 1.14 times 900. The runner reports the hops in every target file. It does not retune the 1.2 offer to chase 1,026. The score does not open or close a payment target.

Families 1–13 and families 14–16 are two cohorts in every file. The score is accepts and attempts for each cohort. Mini's file carries landed hops per minute for each cohort. A higher fee is ahead only when its accept share is higher. The file says the two shares. It does not add a sentence that the higher fee left the mempool. At 1.2 hop/s the HOLD-4 minute holds at most about 72 hops per family. The file says a cohort gap in that minute is thin.

## A payment

The desk file records submit-OK, the attempts, and the rejects, as counts per minute. Rejects are split into rate and full. Per cohort, per minute, it also records submitted-OK not yet landed. That is the waiting count. Per public node, per minute, it records a local number and the counts: synced, DAA, submit-OK, rejects split into rate and full, dropped sockets, and answer time. No names. Submit-to-landing is matched on the desk. The file gets the median and the slow tail per cohort per target. An id used in the match stays off the repo. The file is the sender log. It is not a chain count. A scored file opens with `MET` or `NOT MET`. The HOLD-4 file opens with `OBSERVATION`.

Mini's file is the chain count. It counts accepted hops and the non-coinbase transactions the Mini node accepted in the minute. That number includes base load. It is the only chain reading on try 1. It is not averaged with the desk or the bot. On HOLD-4, Mini writes `TWO SENDERS` only when the bot file is on origin and its line is not `NO SEND`. A `NO SEND` line is `ONE SENDER` plus that one word. If the bot file and [logs/BOT-HALT.md](../logs/README.md) are both absent 10 minutes after the desk's HOLD-4 file is on origin, Mini writes `ONE SENDER` and `bot-file-absent`. Mini does not republish. Scored files publish when the desk's matching file is on origin. HOLD-4 waits for that bound.

The bot file records the bot's own submit-OK, attempts, and rejects for that one minute. If the bot did not send, the line is `NO SEND` and one word: `no-free-node`, `suspend`, `coins-short`, or `halt`. It is not added to Mini's count.

A minute not read in full stays marked. The gap is not filled. Hops and payments after a phase are listed apart, under the next file if they fall in it.

## Where the files go

| Target | Desk | Mini | Bot |
|---|---|---|---|
| One third, first | counts/desk/HOLD-1.md | counts/mini/HOLD-1.md | |
| Two thirds | counts/desk/HOLD-2.md | counts/mini/HOLD-2.md | |
| Three thirds | counts/desk/HOLD-3.md | counts/mini/HOLD-3.md | |
| Four thirds, one minute | counts/desk/HOLD-4.md | counts/mini/HOLD-4.md | counts/bot/HOLD-4.md |
| One third, again | counts/desk/RETURN.md | counts/mini/RETURN.md | |

Each runner publishes its own file when that step closes. One commit. The other machine's folder stays untouched. On a scored step, the minutes before the three clean ones stay in the same file. HOLD-4 is the one sample minute.

## When the targets are met

[logs/METHOD.md](../logs/README.md) leads with the accepted hops per cohort and the payment accepts per target. It compares the two cohorts' accept shares at HOLD-1, HOLD-3, the HOLD-4 minute, and RETURN. It sets the waiting count next to the landed-hop gap for HOLD-3 and the HOLD-4 minute, and it says whether families 1–13 were waiting while families 14–16 landed. If the two cohorts did not share one node set, or the rates were one rate, or the funding coins were not one size, it says so and does not call the fee the whole cause. It records the time from the end of the HOLD-4 minute until the waiting count is back to the last HOLD-1 minute. It lists the bot as its own payment sender at 150, or `NO SEND`. Desk payments at 150 stay the desk's row. Then the misses and the fixes. Then the On origin time of each count file. tn-master links that page when RETURN is on origin. [logs/FIXES.md](../logs/README.md) holds each repair: what failed, what changed, and why.
