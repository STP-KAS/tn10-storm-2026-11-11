> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Counts only.

# Logs

| File | Who writes it | When |
|---|---|---|
| MINI-ARMED.md | Mini's runner | before 11:30 UTC on Wed 11 Nov 2026. One line: `MINI_ARMED` and a UTC timestamp |
| FIXES.md | the desk runner | each time a target misses and a repair is applied. One line: UTC time, what failed, what changed, why |
| METHOD.md | the desk runner | when RETURN is on origin, met or `NOT MET` |
| BOT-HALT.md | the operator | one line, any time, to stop the bot. Absent until the operator writes it |

MINI-ARMED.md, FIXES.md, and METHOD.md are absent until those runners write them. BOT-HALT.md is absent until the operator writes it. The bot's runner reads it from origin and stops.

FIXES.md is counts only. A repair is logged before the sender is changed. The fee, the offer number, and the plan pages stay as they were at 11:20 UTC.

METHOD.md leads with accepted hops per cohort and payment accepts per target. It compares cohort accept shares at HOLD-1, HOLD-3, the HOLD-4 minute, and RETURN. It sets the waiting count next to the landed-hop gap for HOLD-3 and HOLD-4, and it says whether families 1–13 were waiting while families 14–16 landed. If the cohorts did not share one node set, or the rates were one rate, or the funding coins were not one size, it says so and does not call the fee the whole cause. It records the time from the end of the HOLD-4 minute until the waiting count is back to the last HOLD-1 minute. It lists the bot as its own payment sender at 150, or `NO SEND`. Desk payments at 150 stay the desk's row. Then the misses and the fixes. Then the On origin time of each count file. tn-master links it when the run closes. The plan pages stay as they were at 11:20 UTC. A fee estimate is not a row in this file.
