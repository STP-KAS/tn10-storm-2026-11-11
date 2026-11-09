> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Counts only. No key, seed, txid, covenant id, address, host, or port.
>
> The desk's sender log will live here. It is not a chain count. Mini does not write this folder. The paste is [GO-DESK.md](../../GO-DESK.md).

# Desk sender log

The files are absent until each phase closes. A skipped phase is still a file: `SKIP`, the UTC time, and the reason.

| File | Phase |
|---|---|
| QUIET.md | 11:55 UTC until the quiet phase ends |
| HOLD-1.md | one third, 1,013 tx/s |
| HOLD-2.md | two thirds, 2,027 tx/s |
| HOLD-3.md | three thirds, 3,040 tx/s |
| HOLD-4.md | four thirds, 4,053 tx/s |
| DOWN.md | step-down to 1,013 tx/s |
| RECOVERY.md | two hours at 1,013 tx/s, families still on |

A row is the offer commanded, the attempts, and the rejects. Families 1–13 and 14–16 are separate. Mini's folder is the chain count. A minute not read in full stays marked. The gap is not filled.

The runner resolves git once, keeps that full path, and pushes one file per phase. Mini's folder is [../mini/README.md](../mini/README.md).
