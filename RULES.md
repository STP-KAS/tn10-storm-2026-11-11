> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only. Counts only.
>
> This page is the rule. It does not start a machine.

# Rules

The headmaster rule is [tn-master docs/NEURON.md](https://github.com/STP-KAS/tn-master/blob/main/docs/NEURON.md). A chat note does not replace that page or this one.

This repo is one neuron. It is not a restart of Tuesday and not a restart of the 8 Nov confirmation.

## Who publishes

The desk sends the sixteen families for the whole clock, sends payments up to 2,027 tx/s, and counts. The desk runner publishes one file under [counts/desk/](counts/desk/README.md) when each phase closes.

Mini counts and does not send. Mini's runner publishes the same phases under [counts/mini/](counts/mini/README.md). Each machine writes only its own folder. The chat does not publish either folder. The bot does not write them.

| File | What it covers |
|---|---|
| QUIET.md | 11:55 UTC until the quiet phase ends |
| HOLD-1.md | the one-third offer, from the command through the hold or the short |
| HOLD-2.md | two thirds |
| HOLD-3.md | three thirds |
| HOLD-4.md | four thirds |
| DOWN.md | the step back to one third |
| RECOVERY.md | two hours at one third, families still on |

A skipped phase is still a file. The file is one line: `SKIP`, the UTC time, and the reason. The runner pushes it.

A hop is in the file when the accepting block's header time is inside that phase. The row does not carry a txid, a key, a seed, an address, a host, a port, or a covenant id. The family label and the cohort, floor or double, may sit on the row. The accepting block hash may sit on the row. A minute that was not read in full stays marked. The gap is not filled. The two readings are not averaged.

## Hashes

The desk writes [hashes/SIXTEEN.md](hashes/README.md) before the 12:00 UTC send. Fixed is the local write time. On origin is the commit time of the commit that put the rows on GitHub. After that push succeeds, the same runner reads the time from origin and writes it into the file, then pushes that one line. The time comes from origin. A file with rows and no On origin line is not proof. No proved file, no send.

One genesis. The same sixteen families run until recovery ends. A later phase does not publish a second hash file and does not spend a new genesis coin.

## Git

Call git by its full path. Keep the errors. Empty output is a failed read. Read once more with the same path. If that read fails too, stop. One commit per file that just closed. If the push fails, try the same push once more. Then stop and say the git error.

## One runner

One runner on the desk. One runner on Mini. One runner on the bot for the payment share in [plan/PLAN.md](plan/PLAN.md). The runner is a process with a log. The chat is not the runner. A second runner is a fault. A scheduled task is not the arm.

The operator arms the machine. He sends the matching paste. Until that send, the machine waits.

The pastes also wait for the line `REVIEW_CLOSED` in [prompts/REVIEW.md](prompts/REVIEW.md). Until that line is in the file, a paste does not start a runner.

## This clock

The day is Wed 11 Nov 2026. Start is 12:00 UTC (13:00 CET). A phase that has not opened by the latest minute in [plan/PLAN.md](plan/PLAN.md) is skipped. The clock is not moved. Recovery's latest start is 16:30 UTC. The publish is finished by 18:45 UTC.

## When the clock closes

The desk runner writes [logs/METHOD.md](logs/README.md). Success and failure both get that file. The same runner then updates tn-master in the same hour: the index row, the history page, and the timeline line, linking this method file. The plan pages and the pastes stay as they were at 11:20 UTC. A miss is a row. The row is not removed.

If that tn-master push fails, say the git error. Leave the local commit. Do not start another runner to finish the sentence.
