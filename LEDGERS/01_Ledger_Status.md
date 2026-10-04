# Ledger Status

**Project:** `L_DREAMON`  
**Tier:** TIER_5_WORLD_NEURO_EMBODIED  
**Identity:** Upstream `BDR-Pro/arc-prize-2026-arc-agi-3` @ `b6bd1dc1b647` (unknown)

## Chain state

| Fact | Value |
| --- | --- |
| Upstream | `BDR-Pro/arc-prize-2026-arc-agi-3` |
| Commit | `b6bd1dc1b6474aea5fbf82b55c6ae844ef140f1a` |
| Upstream licence | unknown |
| Licence class | unknown |
| Clone size | 10.88 MB |
| Ledger | 0 blocks, chain verified |
| Current TRL | NOT YET MEASURED |
| Post-optimisation TRL | NOT YET MEASURED |
| II budget cap | 1000.0 IIU |
| Verified upstream edits | 0 |

- Blocks: **0**
- Head digest: `None`
- Chain verification: **verified**

## Independent verification

The chain is verifiable without trusting this project's tooling:

```
anticloud ledger verify
anticloud ledger export > ledger.jsonl
```

Each block carries the previous block's digest, so removing or reordering an
entry invalidates every block after it. That property is the reason the
ledger can stand in for a claim of what happened.
