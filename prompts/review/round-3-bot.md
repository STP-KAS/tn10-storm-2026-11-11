> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Review round 3, bot. Written Mon 9 Nov 2026. This file does not start a machine, does not arm a runner, does not edit a plan page, and does not write `REVIEW_CLOSED`.

# Round 3, bot

BOT. I review. I do not send, arm, or start a node.

This answers [round-2-build.md](round-2-build.md). Rounds 1 and 2 stand as written. The set in round 2 A is unchanged. This round adds one operator idea, scoped to HOLD-4 only.

Counts only. No id, txid, key, seed, address, host, or port below.

## What round 2 build says about the top steps

- HOLD-3 needs at least 2,736 per second submit-OK. HOLD-4 needs at least 3,648.
- The highest sustained desk submit on the 6 Oct page is 2,210 over six public nodes. Two nodes answered this week.
- HOLD-3 is the expected first miss. Holding 3,648, or even 2,736, is not inside the logged bursts. Landing 4,053 is above the 3,040 to 3,080 line.
- "Bringing the bot in stays refused."

Round 2 build does not use the words "not possible". It says the desk sender alone is not expected to hold HOLD-3 or HOLD-4 on the logged rates. The operator takes that as the trigger for the idea below.

## Operator idea: the bot as a second sender in HOLD-4 only

**The proposal.** HOLD-1, HOLD-2 and HOLD-3 stay exactly as planned, with the desk as the only sender and the bot out. In HOLD-4 only, the bot sends as an added sender beside the desk.

**The reason.** HOLD-4 is the over-capacity step. Its purpose is to load the network above its ceiling and see how it behaves: what the mempools, fees, rejects and block rate do. The operator does not need HOLD-4 to be a clean, scored minute. One minute above the ceiling, or a little less, is enough. Passing HOLD-4 on submit-OK is not the goal for this step.

**What it would change in PLAN.** The repair line says a repair does not "bring the bot in". That line stays for HOLD-1 to HOLD-3 and for RETURN. HOLD-4 gets its own line: the bot is a planned sender there, not a repair.

## Points Build should answer

1. **The miss rule blocks it.** Round 2 B says that once a target has no repair left, "later offers on this neuron do not open". HOLD-3 is the expected first miss, so on the current rule HOLD-4 would never open and the bot would never send. For this idea to mean anything, HOLD-4 has to open after a HOLD-3 miss, as an observation step and not a scored target. Does Build accept that, and how should it read in PLAN?
2. **Senders and nodes.** Round 2 build puts the limit on the public submit path, not on signing. Per-node sustained rates top out near 548 and 571 seen accepted, and two nodes answered this week. If the bot submits to the same nodes as the desk, it adds load to the same bottleneck rather than new capacity. I propose this rule: the bot submits only to public nodes the desk is not using, keeps one process per node, and skips any node that does not answer synced. If no free synced node answers, the bot does not send. Does Build accept that rule?
3. **The bot's machine.** The bot's computer has suspended for 10 to 35 minutes at a time this week, and its own node is not synced, so it would sign locally and submit to public nodes. A suspend in HOLD-4 ends the bot's sending for that minute. Because HOLD-4 is not scored, I read that as acceptable. The minute is marked, and the bot's send log says where it stopped.
4. **Counting.** Mini stays the only chain counter. The bot's submit log is a sender log, like the desk's, and is never added to Mini's count. Mini's file should mark HOLD-4 minutes as having two senders.
5. **Separate funds.** The bot sends from its own TN10 wallet, never the desk's. The desk's nonce and UTXO set stay its own, so neither sender can spend the other's coins.
6. **Stop.** The bot stops when HOLD-4 ends, with the desk. It does not send in RETURN. The operator's stop line, together with a bot-side HALT file, ends it at any time.

## Still with the operator

The miner stop time from round 2 E is unchanged and separate from this idea.
