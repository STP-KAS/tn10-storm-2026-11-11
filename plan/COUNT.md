> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · This page does not start a machine.

# Count

The file clock is the accepting block's header time. The desk's notice time is not the clock. Mini's receive time is not the clock.

## A hop

An accepted hop landed in a block. Genesis, a conflicting spend, an already-spent input, and an orphan are not hops. They are listed apart. Attempts come from the desk sender log as counts. Attempts are not on chain and they are not ids.

The quiet goal is 1,026 accepted hops per family in one 900-second window. That number is 1.14 times 900. It is the goal of the quiet phase. It does not stop a later hold. During the holds, the step-down, and the recovery, the runner reports the hops. It does not retune the 1.2 offer to chase 1,026.

Families 1–13 and families 14–16 are two cohorts in every file. The score is accepts and attempts for each cohort. A higher fee is ahead only when its accept share is higher. The file says the two shares. It does not add a sentence that the higher fee left the mempool.

## A payment

The desk file counts the desk's own payment accepts and rejects, and the bot file is not a count. The desk runner also records the offer it commanded and the offer the bot reported, as counts per minute.

Mini's file counts non-coinbase transactions the Mini node accepted in the minute. That number includes base load. It is Mini's reading. It is not averaged with the desk.

A minute not read in full stays marked. The gap is not filled. Hops and payments after a phase are listed apart, under the next file if they fall in it.

## Where the files go

| Phase | Desk | Mini |
|---|---|---|
| Quiet | counts/desk/QUIET.md | counts/mini/QUIET.md |
| One third | counts/desk/HOLD-1.md | counts/mini/HOLD-1.md |
| Two thirds | counts/desk/HOLD-2.md | counts/mini/HOLD-2.md |
| Three thirds | counts/desk/HOLD-3.md | counts/mini/HOLD-3.md |
| Four thirds | counts/desk/HOLD-4.md | counts/mini/HOLD-4.md |
| Step-down | counts/desk/DOWN.md | counts/mini/DOWN.md |
| Recovery | counts/desk/RECOVERY.md | counts/mini/RECOVERY.md |

Each runner publishes its own file when the phase closes. One commit. The other machine's folder stays untouched.

## After the clock

[logs/METHOD.md](../logs/README.md) leads with the accepted hops per cohort and the payment accepts per step. Then the misses, the shorts, and the skips. Then the On origin time of each count file. tn-master links that page the same day, success or failure.
