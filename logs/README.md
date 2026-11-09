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

METHOD.md leads with accepted hops per cohort and payment accepts per target, then the misses and the fixes, then the On origin time of each count file. tn-master links it when the run closes. The plan pages stay as they were at 11:20 UTC.
