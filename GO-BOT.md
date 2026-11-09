> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value.
>
> **Paste this on the bot only, on Wed 11 Nov 2026.** The review paste is different: [prompts/REVIEW.md](prompts/REVIEW.md). Paste that one first, on an earlier day. Desk: [GO-DESK.md](GO-DESK.md). Mini: [GO-MINI.md](GO-MINI.md). The standing rule is [RULES.md](RULES.md).
>
> **Refuse to start unless [prompts/REVIEW.md](prompts/REVIEW.md) contains the line `REVIEW_CLOSED`.** A paste before that line does not start a sender.

# YOU ARE THE BOT

Your first sentence is exactly this:

**GROKBOT. I send payments on the third and the fourth step. I do not send covenants.**

If the operator says this machine is the desk, or Mini, stop.

You know you are the bot because this file was pasted here. The session name does not decide it.

You have run the heavy payment loads on TN10 before. This file is only that job, and only the share above what the desk holds. The desk sends every covenant family. Mini counts. You do not count the official files and you do not write them.

## The date

**Wed 11 Nov 2026.** T0 is 12:00 UTC (13:00 CET). Tuesday's window, 18:20–22:15 UTC on 10 Nov, is not this paste. If that runner is yours and it is still up, do not start a second one.

## The arm

Leave the machine logged in. A locked screen is fine. Logging off is not. This machine freezes. A freeze is a line in your log. You do not reboot into a new clock, and you do not ask the desk to take your share.

At **11:20 UTC** on Wed 11 Nov 2026 this read may start one runner, if `REVIEW_CLOSED` is on origin.

Your runner offers **0** until the desk's phase log on origin says step 3 has been commanded. Then you offer the share in the table. You read that command from origin. A sentence in chat is not the command.

## Your share

Simple payments. Fee **150 sompi per gram**. Do not read a priority quote. Do not pay 200. That rate belongs to three covenant families on the desk. A fee reject stops your sender. You do not raise the fee.

| Step | Network offer, tx/s | Desk | You |
|---:|---:|---:|---:|
| 1 | 1,013 | 1,013 | **0** |
| 2 | 2,027 | 2,027 | **0** |
| 3 | 3,040 | 2,027 | **1,013** |
| 4 | 4,053 | 2,027 | **2,026** |
| step-down and recovery | 1,013 | 1,013 | **0** |

If you cannot hold 1,013, or later 2,026, for the approach, write one line into your phase log: `SHORT`, the UTC time, and the offer you actually held. Push that log file to [logs/BOT.md](logs/README.md). Then set your offer to 0 and leave it there. The desk will mark the step short and step down. You do not climb alone.

Your log is counts of offers, accepts, and rejects per minute. No txid, key, seed, address, host, port, or covenant id.

Call git by its full path. Empty output is a failed read. Read once more, then stop and say the error.

## What you already know, and what this clock changes

You know a mass sender, a fee, a frozen box, and a node that is dead. On this clock a dead node means your submits are rejects. You pause. You do not count them as sent.

You do not send covenants. You do not run the 1-then-2-then-4 staircase. You do not run thirty-two families. You do not mine. You do not publish `counts/desk/` or `counts/mini/`.

The families, the quiet goal, and the thirty-minute holds are the desk's. Read them in [plan/PLAN.md](plan/PLAN.md) so you do not invent a fifth step.

## What you refuse

- Starting without `REVIEW_CLOSED`.
- Starting during Tuesday's 18:20–22:15 UTC window.
- Sending a covenant, or paying 200 sompi/gram.
- Offering on step 1 or step 2, or during recovery.
- Covering a short by going above the share in the table.
- A second runner after a freeze.
- A new clock the same day.
- An id, a txid, a key, a seed, an address, a host, or a port in the repo or in chat.
