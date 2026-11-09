> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · This page does not start a machine.

# Count

The file clock is the accepting block's header time. The desk's notice time is not the clock. Mini's receive time is not the clock.

## A hop

An accepted hop landed in a block. Genesis, a conflicting spend, an already-spent input, and an orphan are not hops. They are listed apart. Attempts come from the desk sender log as counts. Attempts are not on chain and they are not ids.

1,026 accepted hops per family in one 900-second window is a score. That number is 1.14 times 900. The runner reports the hops in every target file. It does not retune the 1.2 offer to chase 1,026. The score does not open or close a payment target.

Families 1–13 and families 14–16 are two cohorts in every file. The score is accepts and attempts for each cohort. A higher fee is ahead only when its accept share is higher. The file says the two shares. It does not add a sentence that the higher fee left the mempool.

## A payment

The desk file records the offer the desk commanded, the attempts, and the rejects, as counts per minute. It is the sender log. It is not a chain count.

Mini's file is the chain count. It counts accepted hops and the non-coinbase transactions the Mini node accepted in the minute. That number includes base load. It is the only chain reading on try 1. It is not averaged with the desk.

A minute not read in full stays marked. The gap is not filled. Hops and payments after a phase are listed apart, under the next file if they fall in it.

## Where the files go

| Target | Desk | Mini |
|---|---|---|
| One third, first | counts/desk/HOLD-1.md | counts/mini/HOLD-1.md |
| Two thirds | counts/desk/HOLD-2.md | counts/mini/HOLD-2.md |
| Three thirds | counts/desk/HOLD-3.md | counts/mini/HOLD-3.md |
| Four thirds | counts/desk/HOLD-4.md | counts/mini/HOLD-4.md |
| One third, again | counts/desk/RETURN.md | counts/mini/RETURN.md |

Each runner publishes its own file when that target is met. One commit. The other machine's folder stays untouched. The minutes before the three clean ones stay in the same file.

## When the targets are met

[logs/METHOD.md](../logs/README.md) leads with the accepted hops per cohort and the payment accepts per target. Then the misses and the fixes. Then the On origin time of each count file. tn-master links that page when RETURN is on origin. [logs/FIXES.md](../logs/README.md) holds each repair: what failed, what changed, and why.
