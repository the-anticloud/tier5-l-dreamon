# 3-Seed Simulation — L_DREAMON

**Seeds:** `77622` · `8959` · `43158`

**Seed method:** `sha256("L_DREAMON")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `L_DREAMON`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 6.994 | 0.1589 | ±0.3114 |
| throughput_tokens_per_sec | 357.6333 | 27.2769 | ±53.4627 |
| p50_latency_ms | 46.46 | 4.0215 | ±7.8821 |
| p99_latency_ms | 106.0233 | 11.1548 | ±21.8634 |
| ttft_ms | 28.5433 | 4.002 | ±7.8439 |
| mmlu_proxy | 0.6922 | 0.0305 | ±0.0598 |
| hellaswag_proxy | 0.7906 | 0.0328 | ±0.0643 |
| truthfulqa_proxy | 0.5777 | 0.0446 | ±0.0874 |
| arc_proxy | 0.6958 | 0.0311 | ±0.061 |
| complexity_cyclomatic | 3.9133 | 0.3316 | ±0.6499 |
| maintainability_index | 70.6433 | 4.337 | ±8.5005 |
| security_issues_high | 0.6667 | 0.4714 | ±0.9239 |
| dependency_freshness_pct | 82.0333 | 2.9488 | ±5.7796 |
| test_coverage_pct | 50.1333 | 3.565 | ±6.9874 |
| doc_coverage_pct | 62.0 | 3.879 | ±7.6028 |
| memory_mb | 50.0 | 0.0 | ±0.0 |
| gpu_util_pct | 67.1667 | 3.2294 | ±6.3296 |
| openssf_score | 7.1033 | 0.2963 | ±0.5807 |
| eu_ai_act_compliance_pct | 80.3 | 6.0272 | ±11.8133 |
| slsa_level | 1.0 | 0.0 | ±0.0 |

## Per-Seed Raw Results

| Metric | Seed 77622 | Seed 8959 | Seed 43158 |
|--------|------------|------------|------------|
| trl_score | 7.218 | 6.898 | 6.866 |
| throughput_tokens_per_sec | 365.8 | 386.2 | 320.9 |
| p50_latency_ms | 45.78 | 41.91 | 51.69 |
| p99_latency_ms | 121.69 | 99.79 | 96.59 |
| ttft_ms | 30.8 | 22.92 | 31.91 |
| mmlu_proxy | 0.7353 | 0.6707 | 0.6707 |
| hellaswag_proxy | 0.8185 | 0.8088 | 0.7446 |
| truthfulqa_proxy | 0.5743 | 0.6339 | 0.5248 |
| arc_proxy | 0.7352 | 0.6592 | 0.6929 |
| complexity_cyclomatic | 4.38 | 3.64 | 3.72 |
| maintainability_index | 73.68 | 64.51 | 73.74 |
| security_issues_high | 1 | 0 | 1 |
| dependency_freshness_pct | 79.2 | 86.1 | 80.8 |
| test_coverage_pct | 45.1 | 52.4 | 52.9 |
| doc_coverage_pct | 66.7 | 62.1 | 57.2 |
| memory_mb | 50 | 50 | 50 |
| gpu_util_pct | 64.0 | 65.9 | 71.6 |
| openssf_score | 7.05 | 6.77 | 7.49 |
| eu_ai_act_compliance_pct | 88.8 | 76.6 | 75.5 |
| slsa_level | 1 | 1 | 1 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._