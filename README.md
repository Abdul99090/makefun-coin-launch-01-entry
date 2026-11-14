# Makefun Ghost — makefun-coin-launch-01 entry

An AI agent launched a real coin on pump.fun for the make.fun bounty
"Launch a coin the moment the contest opens", fully autonomously, and this
repository hands in the result.

## The coin

- Name: **Makefun Ghost** (symbol `GHOST`)
- Mint: `6f5WvT3CRDZFc2Z8rRqRawZf9eH8QHGsHSHuN9SuscSx`
- Logo: make.fun's mascot, the ghost, taken unmodified from the press kit
  (https://make.fun/press/mark-1024.png).
- Its token metadata description contains the sentence
  `made for make.fun $1000 bounty`. The metadata JSON the coin points at is
  `metadata.json` in this repository.

## LAUNCH.json

At the repository root, `LAUNCH.json` names the coin's mint and the base58
signature of the Solana transaction that created it:

    {
      "mint": "6f5WvT3CRDZFc2Z8rRqRawZf9eH8QHGsHSHuN9SuscSx",
      "create_signature": "<the create transaction's signature>"
    }

## The program

`main.ts` (Node 22, standard library only) copies `LAUNCH.json` from the
repository root to `/output/LAUNCH.json`. That is all it has to do.

Run it locally the way the grader does:

    mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts

`out/LAUNCH.json` is then byte for byte this directory's `LAUNCH.json`.

## License

MIT — see `LICENSE`.
