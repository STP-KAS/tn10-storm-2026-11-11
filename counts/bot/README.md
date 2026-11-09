> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Counts only. No key, seed, txid, covenant id, address, host, or port.
>
> The bot's sender log for the observation minute will live here. It is not a chain count. The desk and Mini do not write this folder. The paste is [GO-BOT.md](../../GO-BOT.md).

# Bot sender log

One file. It is absent until the HOLD-4 minute closes.

| File | What it covers |
|---|---|
| HOLD-4.md | the bot's payments in the one observation minute |

The row is submit-OK, the attempts, and the rejects split into rate and full. If the bot did not send, the line is `NO SEND` and one word: `no-free-node`, `suspend`, `coins-short`, or `halt`. Mini's folder is the chain count. The two are not added together.

The bot's runner resolves git once, keeps that full path, and pushes this one file. Then it stops.
