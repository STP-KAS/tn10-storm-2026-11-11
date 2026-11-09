> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only. Wed 11 Nov 2026. This page does not start a machine.

# Why this neuron

The quiet covenant runs and the payment floods have been separate nights. This neuron runs them together, from one start, until every payment target is met.

Sixteen covenant families stay on from the first second until the last target is met. The payment offer climbs one third, two thirds, three thirds, and four thirds of the mass-ceiling line, then returns to one third. A target stays open until it is met. The families are still hopping through that return.

## What was read

[kaspa-master-file](https://github.com/STP-KAS/kaspa-master-file) Now, read 9 Nov 2026: the node release is rusty-kaspa **v2.1.0**, tag `01b532e8`, published 2026-09-22. Master is `4863866f` (4 Nov 2026), the merge of [#1164](https://github.com/kaspanet/rusty-kaspa/pull/1164) after [#1152](https://github.com/kaspanet/rusty-kaspa/pull/1152). Those two are an accepting-block transaction RPC and a covenant-id index. They are not a consensus activation and not a governance program. The KIP list on `kaspanet/kips` at `e4ae233` has no governance file.

[KIP-17](https://github.com/kaspanet/kips/blob/e4ae2332117b5cb68bd6188e065ef885b6d17939/kip-0017.md) lists "Congestion control mechanisms" as a use of covenants. That line points at a document. The families this desk can submit are the covenant hops already measured. This neuron submits those.

The running TN10 node stays the binary it is already on. This plan does not switch it to master and does not turn an index on in the middle of a clock.

## The lines this plan keeps

| Line | Number | Source |
|---|---:|---|
| Mass ceiling, low edge | 3,040 payments/s | [FINDINGS 1](https://github.com/STP-KAS/tn-master/blob/main/FINDINGS.md) |
| 11 Oct peak complete minute | 3,583.1 tx/s | [FINDINGS 10](https://github.com/STP-KAS/tn-master/blob/main/FINDINGS.md). A peak minute. The offer is not scaled from it |
| Desk payment hold, 6–7 Oct | 2,207 tx/s seen accepted for 6 h | [tn-master README](https://github.com/STP-KAS/tn-master/blob/main/README.md) |
| Eight families, offer 1.2, cleared 1.14 | slowest about 1.26 hop/s | [FINDINGS 19](https://github.com/STP-KAS/tn-master/blob/main/FINDINGS.md) |
| Sixteen families, confirm desk reading | mean 1,111.1 over 900 s, every family above 1,026 | [confirm method](https://github.com/STP-KAS/tn10-storm-2026-11-08-confirm/blob/main/logs/METHOD.md) |
| Thirty-two families | under 1.14 per family on a quiet network | [FINDINGS 19](https://github.com/STP-KAS/tn-master/blob/main/FINDINGS.md) and the confirm load |
| Minimum relay | 100 sompi per gram | rusty-kaspa v2.1.0. A priority quote is a different number. [FINDINGS 13](https://github.com/STP-KAS/tn-master/blob/main/FINDINGS.md) |

Thirty-two families already miss 1.14 while the network is quiet. They stay on Tuesday's clock. Sixteen is the largest mix this desk has seen clear the 1,026 line. All sixteen are on together. There is no 1-then-2-then-4 staircase on this neuron.

## Fees

Three rates, fixed for the whole run.

| Who | Rate | Sompi per gram |
|---|---:|---:|
| Families 1–13 | 1× minimum relay | 100 |
| Families 14–16 | 2× minimum relay | 200 |
| Payment senders | 1.5× minimum relay | 150 |

Three of sixteen is the largest whole share that stays at or under one fifth. The score is accepted hops and accepted payments for each rate. A higher rate is a cohort in the file. It is not a promise that those transactions leave the mempool.

The node's priority bucket is not read. [FINDINGS 11](https://github.com/STP-KAS/tn-master/blob/main/FINDINGS.md) records a stale mempool quoting 1,644 sompi/gram against a public 100. [FINDINGS 13](https://github.com/STP-KAS/tn-master/blob/main/FINDINGS.md) records that 100× bought nothing more than 10×, and that 150× raised storage mass and lowered throughput.

## What this neuron asks

On a network that is offered 1,013, then 2,027, then 3,040, then 4,053 simple payments per second, do the sixteen families still land, and do families 14–16 land ahead of families 1–13?

The run stays on an offer until three clean minutes land. Then the next offer starts. After 4,053, the offer returns to 1,013 and the families stay on until that target is met. There is no latest minute after the start.

## Who sends

The desk is the only sender. Mini is the only chain counter. The bot stays out of this neuron. The desk node process is stopped for the send, after Tuesday's runner is down, and the senders use public TN10 nodes. The chain data stays. The log is [plan/TRIES.md](plan/TRIES.md). This clock is try 1. Pulse is not asked to count it.

## What stays on its own clock

Tuesday 10 Nov 2026, 19:00 UTC, is [tn10-storm-2026-11-10](https://github.com/STP-KAS/tn10-storm-2026-11-10). File 1 of that count is due Wed 11 Nov 2026 at 12:00 CET (11:00 UTC). This neuron's paste is 11:20 UTC. The list of everything else left off this clock is [plan/LATER.md](plan/LATER.md).
