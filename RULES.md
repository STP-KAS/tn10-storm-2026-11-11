> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only.
>
> This page is the rule. It does not start a machine.

# Rules

The headmaster rule is [tn-master docs/NEURON.md](https://github.com/STP-KAS/tn-master/blob/main/docs/NEURON.md). A chat note does not replace that page or this one.

This repo is one neuron. It is not a restart of Tuesday and not a restart of the 8 Nov confirmation.

## Who publishes

The desk sends the sixteen families until RETURN is met, and sends every payment offer. The desk runner publishes one file under [counts/desk/](counts/desk/README.md) when a scored target closes, met or not met, and when the HOLD-4 minute is done. That file is submit-OK, the attempts, and the rejects split into rate and full. It is the sender log. It is not a chain count.

Mini is the only chain counter. Mini counts and does not send. Mini's runner publishes the same phases under [counts/mini/](counts/mini/README.md). The bot publishes one sender log, [counts/bot/HOLD-4.md](counts/bot/README.md), for the observation minute. Each machine writes only its own folder. The chat does not publish a folder.

| File | What it covers |
|---|---|
| HOLD-1.md | the first one-third offer, from the open through the three clean minutes, or through the repair pass |
| HOLD-2.md | two thirds |
| HOLD-3.md | three thirds, met or `NOT MET` |
| HOLD-4.md | one observation minute at four thirds. The first line is `OBSERVATION` |
| RETURN.md | one third again, families still on, through its three clean minutes, or through the repair pass |

A scored target that is still open has no file. HOLD-3 publishes `NOT MET` when one pass of repairs is done. That file opens HOLD-4. The runner does not leave HOLD-3 open with no file.

A hop is in the file when the accepting block's header time is inside that phase. The row does not carry a txid, a key, a seed, an address, a host, a port, or a covenant id. The family label and the cohort, floor or double, may sit on the row. The accepting block hash may sit on the row. A minute that was not read in full stays marked. The gap is not filled. The two readings are not averaged.

## Hashes

The desk writes [hashes/SIXTEEN.md](hashes/README.md) before the 12:00 UTC send. Fixed is the local write time. On origin is the commit time of the commit that put the rows on GitHub. After that push succeeds, the same runner reads the time from origin and writes it into the file, then pushes that one line. The time comes from origin. A file with rows and no On origin line is not proof. No proved file, no send.

One genesis. The same sixteen families run until the last target is met. A later target does not publish a second hash file and does not spend a new genesis coin.

## Git

Call git by its full path. Keep the errors. Empty output is a failed read. Read once more with the same path. If that read fails too, stop. One commit per file that just closed. If the push fails, try the same push once more. Then stop and say the git error.

## One runner

One runner on the desk. One runner on Mini. One runner on the bot, and it sends payments only in the HOLD-4 minute. The runner is a process with a log. The chat is not the runner. A second runner on the same machine is a fault. A scheduled task is not the arm.

The operator arms the machine. He sends the matching paste. Until that send, the machine waits.

The pastes also wait for the line `REVIEW_CLOSED` in [prompts/REVIEW.md](prompts/REVIEW.md). Until that line is in the file, a paste does not start a runner.

## This clock

The day is Wed 11 Nov 2026. Start is 12:00 UTC (13:00 CET). The hash launch before that start is timed. After the start, the run follows the targets in [plan/PLAN.md](plan/PLAN.md). A scored target stays until it is met or one repair pass is done. HOLD-4 is one minute. The start is not moved.

## When the targets are met

The desk runner writes [logs/METHOD.md](logs/README.md) when RETURN is on origin, and also when RETURN is `NOT MET`. The same runner then updates tn-master: the index row, the history page, and the timeline line, linking that method file. The plan pages and the pastes stay as they were at 11:20 UTC. A miss is a row. The row is not removed. Fixes made during the run are [logs/FIXES.md](logs/README.md).

If that tn-master push fails, say the git error. Leave the local commit. Do not start another runner to finish the sentence.
