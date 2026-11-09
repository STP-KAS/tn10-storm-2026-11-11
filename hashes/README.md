> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only. No covenant id in this folder.
>
> Nothing here is a result yet. The file below is written by the desk runner before the 12:00 UTC send on Wed 11 Nov 2026. Until then it is absent on purpose.

# Hashes

| File | When it has to be here | What it covers |
|---|---|---|
| SIXTEEN.md | before 12:00 UTC, and only after Mini's armed line is on origin | all sixteen families, one genesis, the whole neuron |

Each row is a sha256 of a lowercase hex covenant id, plus the family label and the cohort. Floor is families 1–13. Double is families 14–16. The id stays off this repo. No file, no send.

Fixed is the local write. On origin is the commit time of the rows, read from origin after the push, then written back and pushed. A file with rows and no On origin line is not proof. Empty git output is a failed read. Read once more. If that read fails too, stop.

One hash file for the day. Later phases do not get a second genesis.
