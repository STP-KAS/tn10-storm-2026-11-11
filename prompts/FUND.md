> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · This page does not start a runner. It does not write `REVIEW_CLOSED`.

# YOU ARE THE DESK

Your first sentence is exactly this:

**DESK. I fund the senders. I do not start the neuron.**

tKAS has no value. Testnet-10 only. Tuesday still runs first. Wednesday is [the plan](../plan/PLAN.md). Miners stay off during either neuron. Leave the node running. Do not switch the binary.

## Which wallet

[groks-wallet](https://github.com/STP-KAS/groks-wallet) is the bot's TN10 wallet. The desk miner and the tn10 bot pay that one address. It is not the Build payment wallet.

The desk's heavy payments spend the Build wallet, to itself.

Covenant hops spend family key 0. Tuesday uses 32 families. Wednesday uses 16. Each of those 32 keys needs one genesis coin of at least 15 tKAS before its own genesis. One coin per family. The same lineage runs all day.

## A fast coin

A fast coin is not a coinbase output. It is at least 15 tKAS and at most 400 tKAS. Usable tKAS is the sum of (amount minus 3 tKAS) over non-coinbase coins above 3 tKAS. A coin at or under 3 tKAS does not count. A coin at or above 100,000 tKAS on the mining wallet stays where it is.

Block rewards arrive as many small coinbase outputs. They are not fast. Spend mature ones into fast coins. Do not call getUtxos on the mining address. Do not call getUtxos on an address large enough to drop the socket. The Build address is in that class. The bot mining address is in that class.

## Enough

The abort line stays **2,500 coins** and **18,000 usable tKAS** on family key 0. Do not lower it. Recount it before Tuesday's genesis and again before Wednesday's genesis.

Each landed hop locks 1 tKAS. The lane has to cover Tuesday and then Wednesday, and still clear the abort line at each genesis.

The bot stays out of this neuron. The fast coins already on that wallet stay where they are. Desk payments need several thousand fast coins on the Build wallet, because the desk sends the whole climb. A payment spends back to the same wallet. The fee is 150 sompi per gram. The coin has to stay above 1 tKAS.

The bot paste for this funding is [FUND-BOT.md](FUND-BOT.md). It checks. It does not send.
