# aavegotchi-gotchiverse-skill

Codex skill package for Aavegotchi Gotchiverse player operations on Base mainnet.

## What is included

- `aavegotchi-gotchiverse/SKILL.md`: primary operating guide and runbook.
- `aavegotchi-gotchiverse/references/addresses.md`: canonical contract and token addresses.
- `aavegotchi-gotchiverse/references/subgraph.md`: subgraph queries and discovery workflow.
- `aavegotchi-gotchiverse/references/realm-recipes.md`: realm actions (channel, survey, harvest, equip, move).
- `aavegotchi-gotchiverse/references/installation-recipes.md`: installation crafting, queueing, claiming, upgrades.
- `aavegotchi-gotchiverse/references/tile-recipes.md`: tile crafting, queueing, claiming, placement.
- `aavegotchi-gotchiverse/references/access-rights.md`: parcel access rights and whitelist behavior.
- `aavegotchi-gotchiverse/references/failure-modes.md`: common revert causes and troubleshooting.

## Supported workflows

- Parcel discovery and preflight checks
- Surveying and harvesting alchemica
- Channeling alchemica with altar/cooldown constraints
- Crafting, claiming, and reducing installation/tile queues
- Equipping, unequipping, and moving installations/tiles
- Installation upgrade lifecycle management
- Parcel access-right reads and writes

## Safety defaults

- Default to `DRY_RUN=1` and simulate before any broadcast.
- Verify Base chain ID (`8453`) before transactions.
- Verify `PRIVATE_KEY` maps to `FROM_ADDRESS`.
- Refetch subgraph state and revalidate onchain values before `cast send`.

## Required environment variables

`PRIVATE_KEY`, `FROM_ADDRESS`, `BASE_MAINNET_RPC`, `DRY_RUN`, `REALM_DIAMOND`, `INSTALLATION_DIAMOND`, `TILE_DIAMOND`, `AAVEGOTCHI_DIAMOND`, `FUD`, `FOMO`, `ALPHA`, `KEK`, `GLTR`, `GOTCHIVERSE_SUBGRAPH_URL`, `CORE_SUBGRAPH_URL`

Optional:

- `GOLDSKY_API_KEY` (used when querying auth-gated endpoints)
