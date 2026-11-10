> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Counts only. No key, seed, txid, covenant id, address, host, or port.
>
> Mini's count files will live here. The desk does not write this folder. The paste is [GO-MINI.md](../../GO-MINI.md).

# Mini counts

Five steps. Mini publishes each scored file when the desk's matching file is on origin, including a HOLD-3 file that says `NOT MET`. HOLD-4 waits until the bot file or [logs/BOT-HALT.md](../../logs/README.md) is on origin, or for 10 minutes after the desk's HOLD-4 file, as [GO-MINI.md](../../GO-MINI.md) says. Mini is the only chain counter. The chat does not. On HOLD-4, `TWO SENDERS` only when the bot file is on origin and its line is not `NO SEND`. Otherwise `ONE SENDER`. Mini does not republish.

| File | Target |
|---|---|
| HOLD-1.md | one third, first |
| HOLD-2.md | two thirds |
| HOLD-3.md | three thirds |
| HOLD-4.md | four thirds |
| RETURN.md | one third, again |

Mini's non-coinbase count includes base load. It is the chain reading. The rule is [plan/COUNT.md](../../plan/COUNT.md).
