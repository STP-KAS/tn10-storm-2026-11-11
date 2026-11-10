> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Counts only. No key, seed, txid, covenant id, address, host, or port.
>
> The desk's sender log will live here. It is not a chain count. Mini does not write this folder. The paste is [GO-DESK.md](../../GO-DESK.md).

# Desk sender log

The files are absent until each step closes. A scored target that is still open has no file. A closed miss says `NOT MET`.

| File | Target |
|---|---|
| HOLD-1.md | one third, 1,013 tx/s, first |
| HOLD-2.md | two thirds, 2,027 tx/s |
| HOLD-3.md | three thirds, 3,040 tx/s |
| HOLD-4.md | one observation minute at 4,053 tx/s. The first line is `OBSERVATION` |
| RETURN.md | one third again, 1,013 tx/s, families still on |

A scored file is written when that target is met, or when one pass of repairs leaves it `NOT MET`. The minutes before the close stay in it. HOLD-4 is the one sample minute.

A row is submit-OK, the attempts, and the rejects split into rate and full. Families 1–13 and 14–16 are separate, including the waiting count per minute. Each public node is a local number and a count row. Mini's folder is the chain count. A minute not read in full stays marked. The gap is not filled.

The runner resolves git once, keeps that full path, and pushes one file per phase. Mini's folder is [../mini/README.md](../mini/README.md).
